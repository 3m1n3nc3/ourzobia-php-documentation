.. raw:: html

    <style> 
    	.green {
    		color:green; 
    	} 
    	.reds {
    		color:red; 
    	}  
    </style>

.. role:: green
.. role:: reds
.. role:: raw-html(raw)
   :format: html
 
***********
RESTful API
***********

All requests to our RESTful API are served from the ``/api`` endpoint, the ``/requests`` endpoint will be routed to the ``/api`` endpoint and will be removed in future versions.

============   ========================   ================================  ====================  
Method         Endpoint                   Parameters                        Status Code           
============   ========================   ================================  ====================    
:reds:`POST`   /verify          
                                          **domain:**   
                                          This should be the domain name                         
                                          to verify                                            
                                                                            :green:`200 Success`

                                                                            :reds:`400 Failure`
                                              
:reds:`POST`   /activate            
                                          **domain:**    
                                          This should be the domain name                         
                                          to activate   

                                          **email:**    
                                          Email Address used during 
                                          product creation. 

                                          **code:**    
                                          Purchase Code generated during 
                                          product creation.                                            
                                                                            :green:`200 Success`

                                                                            :reds:`400 Failure`                                    
============   ========================   ================================  ====================    

Activating a Product
====================

To activate a product, make a request to the ``/activate`` endpoint and provide the following parameters:

1. :reds:`domain`: This should be the domain name of the product to activate.
2. :reds:`email`: This should be the Email Address used during the product creation.
3. :reds:`code`: This should be the Purchase Code generated during the product creation.

::

	curl "http://toneflixcode.cf/hubboxx/api/activate?origin=alimontaziba.js" \
	  -X POST \
	  -d "domain=toneflixcode.cf&email=support@toneflixcode.cf&code=EBUVMMUZX" \
	  -H "Referer: http://toneflixcode.cf" \
	  -H "Content-Type: application/x-www-form-urlencoded" 

If the request is successful, you should get a response similar to:

.. code-block:: json 

	{
	 "success": true,
	 "status": "success",
	 "status_code": "200",
	 "message": "Product Successfully Activated!"
	}

If the product is already active, a :green:`202 status_code` will be returned with an ``info`` status.

If the product code is invalid, a :reds:`400 status_code` will be returned with an ``error`` status.


Validating a Product
====================

To validate a product, make a request to the ``/verify`` endpoint and provide the following parameters:

1. :reds:`domain`: This should be the domain name of the product to validate. 

::

	curl "http://toneflixcode.cf/hubboxx/api/verify?origin=alimontaziba.js" \
	  -X POST \
	  -d "domain=toneflixcode.cf" \
	  -H "Referer: http://toneflixcode.cf" \
	  -H "Content-Type: application/x-www-form-urlencoded" 

If the request is successful, you should get a response similar to:

.. code-block:: json 

	{
	 "success": true,
	 "status": "success",
	 "status_code": "200",
	 "message": "Product is Active!"
	}

If the product code is not valid, a :reds:`400 status_code` will be returned with an ``error`` status.