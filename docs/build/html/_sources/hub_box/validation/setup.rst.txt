***********
Add Product
***********

After setting up your product to interface with the API, the next step will be to grant usage access to a customer who has acquired the rights to use your product by adding the product to the validation APIs database.

*Setting up product validation and activation requires you to be looged in as an admin*.

Point your web browser to ``http://yourdomain.com/admin/products/create`` where ``yourdomain.com`` is your actual domain name, or click on ``Products`` > ``Add Product`` on the admin dashboard.

- Enter any name that identifies your product, it will be important to use the same name for all similar products you setup for validation. 
- Enter the customer's email address, this will be required when the customer first attempts to use the product.
- You may skip the domain name, just in case the user want to use one you are not aware of, the system will acquire this during validation and lock the product to that domain.
- The product code will also be required when the customer first attempts to use the product and is automatically generated.
- Set the status to *Active* and click on ``Add``, when you edit a product you can set the status to *Inactive* to prevent validation.


NB: *When you click on* ``Add`` *an associated user account will be generated for the provided email address which the new product will be linked to, if the email address already has an associated account, this process is skipped and the product is directly linked to it*.

After setting up the product, the data you need to give to the user is just the **Email Address** and **Activation Code**, and optionally the **Domain Name**, when a Domain Name is provided script installation will be locked to that domain.