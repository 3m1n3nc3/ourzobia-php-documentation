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

********************
Basic Implementation
********************

This section describes in the most basic form, how to implement product Validation and Activation on your code scripts using HubBox, It is the responsibility of the programmer to choose how to best integrate the validation plugin or implement the validation process without selling out soft spots to malicious individuals.

The validation plugin depends on jQuery and is made up of 3 Javascript files and 1 css files namely:

::

	1. alimon.css
	2. alimon.js
	3. alimontaziba.js
	4. js.cookie.js

You are only required to include the ``alimon.js`` on your script with a ``<script></script>`` tag. 

On the ``<script></script>`` tag you will have to include 3 data attributes.

1. ``data-current="true"``: This will let the plugin know that this is the script referring to the plugin.
2. ``data-endpoint="src"``:reds:`*`: This is the directory endpoint on the domain referenced by the **data-src** where the scripts are served from, this should have an empty string value or left undefined if the plugin is not being served from a CDN. (*Sometimes this could also cause problems even when the plugin is served from a CDN, when this happens, please give this an empty string value or leave it undefined*)
3. ``data-src=""``: This should be the same as the the value of the **src** attribute with leading slash, you can stop at the top directory level and skip the filenames.
4. ``data-api=""``: This should be base url or domain of the API.

The ``src=""`` url should contain the following query strings.

1. ``origin=alimon.js``: This will help prevent the API from logging the validation or activation attempt as a site visit.
2. ``url_var=true``: This is important if your API is not served via CDN, the server will use this find variables that need values changed to reference the APIs server.

This example is all you need to get started:

.. code-block:: html 

   <script src="https://cdn.jsdelivr.net/npm/jquery@3/dist/jquery.min.js"></script>
   <script
   	src="https://cdn.jsdelivr.net/gh/3m1n3nc3/ourzobia-api@1/src/alimon.js?url_var=true&origin=alimon.js"
   	data-current="true"
   	data-endpoint="src"
   	data-src="https://cdn.jsdelivr.net/gh/3m1n3nc3/ourzobia-api@1/src/alimon.js/"
   	data-api="https://api.ourzobiaphp.cf/">
   </script>

The example is hosted on `jsdelivr.net <https://jsdelivr.net>`_ CDN and can be used by simply replacing the value of ``data-api=""`` attribute with the full url from where your API is served from.

.. toctree::
    :glob:
    :titlesonly: