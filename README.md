# E-Commerce WebApp

An E-commerce Website built using React, CommerceJS and Stripe

All the backend is handled by CommerceJS

To learn more about CommerceJS : https://commercejs.com/

Create a lib folder inside the src folder and create a commerce.js file inside it. 

src/lib/commerce.js

Create a .env file in the root directory with the following code:

    REACT_APP_CHEC_PUBLIC_KEY = your commerceJS API key

And inside commerce.js file, write the following code:

    import Commerce from "@chec/commerce.js";

    export const commerce = new Commerce(
        import.meta.REACT_APP_CHEC_PUBLIC_KEY,
        true
    );

In case of Invalid Public API Key Error, edit the commercejs file to :

    export const commerce = new Commerce( "your commerceJS API Key");
