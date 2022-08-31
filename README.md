

# hubspot-ecommerce-sync-boilerplate

**A 2022 Ecommerce Bridge to CRM v3 sync boilerplate postman collection runner**

## Instructions:
**Create Private app in your Husbpot portal with the following scopes: (could be thinned but will need testing):**

 - [ ] integration-sync e-commerce crm.objects.contacts.read
 - [ ] crm.objects.contacts.write crm.schemas.contacts.read
 - [ ] crm.objects.deals.read crm.objects.deals.write
 - [ ] crm.schemas.contacts.write crm.schemas.deals.read
 - [ ] crm.schemas.deals.write crm.objects.line_items.read
 - [ ] crm.objects.line_items.write crm.schemas.line_items.read

**Create new Postman Workspace**

**Create new Postman Environment**

 - [ ] add variable named token with the value of your Hubspot
       private app key

**Import collection into postman**

**Open collection variables:**

    store_id_value:  		Internal name of your new Source Store
    store_id_description:		Description of your new Source Store
    store_id_label:			Visible label of selected Source Store on Hubspot object

    ecommerce_property_group_internal_name: 	Internal name of Ecommerce property group for each object
    ecommerce_property_group_label: 		Label of Ecommerce property group for each object
    
    create_pipeline_flag:		Set to true if you would like to create pipeline using collection runner
    create_properties_flag: 	Set to true if you would like to create properties using collection runner
    create_properties_flag: 	Set to true if you would like to create properties using collection runner
    create_example_objects_flag: 	Set to true if you would like to create example objects using collection runner
    
    pipeline_id:			Leave blank, collection runner will set this based on either the existing or newly created commerce pipeline.
    created_contact_id: 		Leave blank, used for object creation and associations
    created_deal_id: 		Leave blank, used for object creation and associations
    created_product_id: 		Leave blank, used for object creation and associations
    created_line_item_id: 		Leave blank, used for object creation and associations
    

**Open Collection runner:**

Configure Run Settings<br/><br/>
[![4iDMW7.png](https://iili.io/4iDMW7.png)](https://freeimage.host/)<br/>

Run all requests in collection
	 - This will setup pipeline
	 - Create properties
	 - Create example objects with associations
