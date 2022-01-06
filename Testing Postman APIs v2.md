
## Testing Postman APIs (v2)
For all v2 Api and few v1 endpoints which are Address, Billings, Account Details and Orders(Order History) we need to pass bearer token in Authorization


To generate token in postman we have an api in Firebase folder in which v2-AuthToken Validation , we have to pass valid email , password , returnSecureToken which will return token and store globally in postman and applied to all the required APIs

  
 <details><summary>
Search, On_Search APIs need to be checked for postman for, searching for an item by delivery location:
  </summary>

-  The BIAB BAP Hackathon collection must have set the ‘base_url’ under ‘variables’ and initial value and current value must be set as https://qa.api.box.beckn.org/bap

-  For this api user Authentication is not mandatory

-  The search by item and location in Search API needs to be tested at the postman for this step, the command {{base_url}}/client/v1/search needs to be run under POST in Postman by clicking ‘send’

-  There will be search string and delivery location values in the body of the Search API

-  The result of sending of the above mentioned POST command can be seen at the bottom half of the page

-  There will be a message acknowledgement status along with the context (containing domain, country, bap_id, bap_url) with transaction_id and message_id

-  Copy the message_id from here

-  This copied message id must be entered in the ‘Params’ (parameters) part of the On_Search API

-  GET On-Search API needs to be run by clicking ‘send’, result is observed in bottom half of the page

-  The context containing domain country etc is seen again, here it is observed that the message_id is same as the message_id of copied from result of running POST Search API

-  Transaction_id, message_id are some values seen in ‘context’. The ‘message’ in the result contains the providers with their respective id, descriptor, price and other parameters.
</details>
  <details><summary>
Add item to cart and On Get Quote API:
  </summary>

The Add item to cart under Client-v2 Quote needs to be tested at the postman to add items to cart, the command {{base_url}}/client/v2/get_quote and add Bearer-Token in Authorization in needs to be run under POST in Postman by clicking ‘send’

-  There will be array object which has context,message, cart, items, bpp provider seen in the body of the Add item to cart API

-  For this api user Authentication is mandatory for which we need to pass Bearer token in Authorization tab

-  The result of sending of the above mentioned POST command can be seen at the bottom half of the page

-  There will be a array object which has message acknowledgement status along with the context (containing domain, country, bap_id, bap_url) with transaction_id and message_id

-  Copy the message_id from here

-  This copied message id from objects and must be entered in the ‘Params’ (messageIds) with comma separated as a part of the On Get Quote API

-  GET On Get Quote API needs to be run by clicking ‘send’, result is observed in bottom half of the page

-  The context containing domain country etc is seen again, here it is observed that the message_id is same as the message_id of copied from result of running POST Add item to cart API

-  Transaction_id, message_id are some values seen in ‘context’. The ‘message’ in the result contains the quote, provider id, descriptor, provider location and other parameters.
</details>
<details><summary>
Search by Category: Test By Category and On_Search APIs
  </summary>

-  The search string with delivery location, category id category name are seen in Client-v2 By Category API under Search folder, the command {{base_url}}/client/v1/ needs to be run under POST in Postman by clicking ‘send’

-  The result of sending of the above mentioned POST command can be seen at the bottom half of the page

-  There will be a message acknowledgement status along with the context (containing domain, country, bap_id, bap_url) with transaction_id and message_id

-  Copy the message_id from here

-  This copied message id must be entered in the ‘Params’ (parameters) part of the By Category API

-  GET On_Search API needs to be run by clicking ‘send’, result is observed in bottom half of the page

-  The context containing domain country etc is seen again, here it is observed that the message_id is same as the message_id of copied from result of running POST By Category API

-  Transaction_id, message_id are some values seen in ‘context’. The ‘message’ in the result contains the types of catalogs.
</details>
  
  
  
  
<details><summary>Billing and Shipping details : Test Initialize and On Initialize API:
  </summary>

The Initialize Order API under Client-v2 Initialize folder needs to be tested at the postman to initialize an order, the command {{base_url}}/client/v2/initialize_order and and add Bearer-Token than needs to be run under POST in Postman by clicking ‘send’

-  Look at the body of the Initialize Order API to know more about the fields in it

-  The result of sending of the above mentioned POST command can be seen at the bottom half of the page

-  There will be a array of object which has message acknowledgement status along with the context (containing domain, country, bap_id, bap_url) with transaction_id and message_id

-  Copy the message_id from here

-  This copied message ids must be entered in the ‘Params’ (messageIds) with comma separated and also add Bearer-Token to the On Initialize API

-  GET On Initialize API needs to be run by clicking ‘send’, result is observed in bottom half of the page

-  The context containing domain country etc is seen again, here it is observed that the message_id is same as the message_id of copied from result of running POST Initialize Order API

-  Transaction_id, message_id are some values seen in ‘context’. The ‘message’ in the result contains the order, order provider,provider location, billing and delivery information
</details>
<details><summary>
Proceed to pay: Test Client confirm_order and client onconfirm_order API:
  </summary>

The Client Confirm_Order API under Client-v2 confirm folder needs to be tested at the postman to initialize an order, the command {{base_url}}/client/v2/confirm_order and also add Bearer-Token which then needs to be run under POST in Postman by clicking ‘send’

-  Look at the body of the confirm order API to know the fields in it

-  The result of sending of the above mentioned POST command can be seen at the bottom half of the page

-  There will be a array of object which has message acknowledgement status along with the context (containing domain, country, bap_id, bap_url) with transaction_id and message_id

-  Copy the message_id from here

-  This copied message id must be entered in the ‘Params’ (messageIds) with comma separated and also add Bearer-Token to the on_confirm API

-  GET on_confirm API needs to be run by clicking ‘send’, result is observed in bottom half of the page

-  Transaction_id, message_id are some values seen in ‘context’. The context containing domain country etc is seen again, here it is observed that the message_id is same as the message_id of copied from result of running POST confirm API
</details>
<details><summary>
Order status: Test Client status_order and client onstatus_order API:
  </summary>

The Client order_status API under Client-v2 Status folder needs to be tested at the postman to initialize an order, the command {{base_url}}/client/v2/order_status and also add Bearer-Token needs to be run under POST in Postman by clicking ‘send’

-  Look at the body of the order_status API to know the fields in it

-  The result of sending of the above mentioned POST command can be seen at the bottom half of the page

-  There will be a array of object which has message acknowledgement status along with the context (containing domain, country, bap_id, bap_url) with transaction_id and message_id

-  Copy the message_id from here

-  This copied message id must be entered in the ‘Params’ (messageIds) with comma separated and also add Bearer-Token to the on_order_status API

-  GET on_order_status API needs to be run by clicking ‘send’, result is observed in bottom half of the page

-  Transaction_id, message_id are some values seen in ‘context’. The context containing domain country etc is seen again, here it is observed that the message_id is the same as the message_id copied from the result of running POST order_status API. In ‘message’ order, provider, billing and fulfillment, item, payment values would be seen
</details>
<details><summary>
Track order: Test Client track and client ontrack_order API
  </summary>

The Client track_orderAPI under Client-v2 Track folder needs to be tested at the postman to initialize an order, the command {{base_url}}/client/v2/track and also add Bearer-Token which needs to be run under POST in Postman by clicking ‘send’

-  Look at the body of the track API to know the fields in it

-  The result of sending of the above mentioned POST command can be seen at the bottom half of the page

-  There will be a array of object which has message acknowledgement status along with the context (containing domain, country, bap_id, bap_url) with transaction_id and message_id

-  Copy the message_id from here

-  This copied message id must be entered in the ‘Params’ (messageIds) with comma separated and also add Bearer-Token to the on_track API

-  GET on_track API needs to be run by clicking ‘send’, result is observed in bottom half of the page

-  Transaction_id, message_id are some values seen in ‘context’. The context containing domain country etc is seen again, here it is observed that the message_id is the same as the message_id copied from the result of running POST track API. In ‘message’ status, url will be seen
</details>
<details><summary>
Order History: Test Order History API
  </summary>

The Client orders history API under Client-v2 Orders folder needs to be tested at the postman to get order history information, the command {{base_url}}/client/v1/order and also add Bearer-Token which needs to be run under GET in Postman by clicking ‘send’

-  Look at the params of the order API to know the fields in it

-  We can either pass orderId param to see the order specific history

-  Or We can pass parentOrderId to see all the individual orders under parent Order

-  We can handle pagination using skip and limit

-  The result of sending of the above mentioned GET command can be seen at the bottom half of the page

-  Response has array object in which each object has provider, items array, billing , fulfillment, quote, payment, id, state, transation_id,message_id, parent_order_id
</details>
  
<details><summary>
Delivery Address: Test Delivery Address API
  </summary>

The Client delivery address API under Client-v2 Accounts/Delivery Address folder needs to be tested at the postman to add delivery address, the command {{base_url}}/client/v1/delivery_address and also add Bearer-Token which needs to be run under POST in Postman by clicking ‘send’

-  Look at the body of the delivery_address API to know the fields in it

-  The result of sending of the above mentioned POST command can be seen at the bottom half of the page

-  There will be object which has id, descriptor, gps, default_address, address fields

-  GET delivery_address API needs to be run with only Bearer-Token to get all the delivery address by clicking ‘send’, result is observed in bottom half of the page
</details>
  
<details><summary>
Add Billings: Test Billings API
  </summary>

The Client billing address API under Client-v2 Accounts/Billings folder needs to be tested at the postman to add delivery address, the command {{base_url}}/client/v1/billing_details and also add Bearer-Token which needs to be run under POST in Postman by clicking ‘send’

-  Look at the body of the billing_details API to know the fields in it

-  The result of sending of the above mentioned POST command can be seen at the bottom half of the page

-  There will be object which has id, name, phone, organization, address, email, tax_number, location_id fields

-  GET billing_details API needs to be run with only Bearer-Token to get all the billing details by clicking ‘send’, result is observed in bottom half of the page
</details>
<details><summary>
Update Account Info: Test Account Info API
  </summary>

The Client Account Info API under Client-v2 Accounts/AccountDetails folder needs to be tested at the postman to update user account information, the command {{base_url}}/client/v1/account_details and also add Bearer-Token which needs to be run under POST in Postman by clicking ‘send’

-  Look at the body of the account_details API to know the fields in it

-  The result of sending of the above mentioned POST command can be seen at the bottom half of the page

-  There will be object which has user_phone, user_email, user_name

-  GET account_details API needs to be run with only Bearer-Token to get all the account information by clicking ‘send’, result is observed in bottom half of the page
  </details>
