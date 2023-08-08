# E-Commerce WebApp

An E-commerce Website built using React, CommerceJS and Stripe

All the backend is handled by CommerceJS and all of the payment process is handled by Stripe

To learn more about CommerceJS : https://commercejs.com/
To learn more about Stripe : https://stripe.com/

Create a lib folder inside the src folder and create a commerce.js and stripe.js file inside it.

src/lib/commerce.js
src/lib/stripe.js

Create a .env file in the root directory with the following code:

    REACT_APP_CHEC_PUBLIC_KEY = your sandbox public commerceJS API key
    REACT_APP_STRIPE_PUBLIC_KEY = your publishable stripe API key

Inside commerce.js file, write the following code:

    import Commerce from "@chec/commerce.js";

    export const commerce = new Commerce(
        import.meta.REACT_APP_CHEC_PUBLIC_KEY,
        true
    );

And inside stripe.js file, write the following code:

    import { loadStripe } from "@stripe/stripe-js";

    export const stripePromise = loadStripe(
        import.meta.REACT_APP_STRIPE_PUBLIC_KEY
    );

In case of Invalid Public API Key Error, edit the commerce.js file to :

    export const commerce = new Commerce( "your sandbox public commerceJS API Key");

In case of value for stripe() apikey should be a string Error, edit the stripe.js file to :

    export const stripePromise = loadStripe("your publishable stripe API key");
