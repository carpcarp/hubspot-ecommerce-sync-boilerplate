# hubspot-ecommerce-sync-boilerplate
A 2022 Ecommerce Bridge to CRM v3 sync boilerplate postman collection runner

Instructions:
Create Private app in your Husbpot portal with the following scopes: (could be thinned but will need testing):
integration-sync
e-commerce
crm.objects.contacts.read
crm.objects.contacts.write
crm.schemas.contacts.read
crm.objects.deals.read
crm.objects.deals.write
crm.schemas.contacts.write
crm.schemas.deals.read
crm.schemas.deals.write
crm.objects.line_items.read
crm.objects.line_items.write
crm.schemas.line_items.read

Create new Postman Workspace

Create new Postman Environment
- add variable named token and with the value of your Hubspot private app key 

Import collection into postman

Open collection variables:
store_id_value: internal name of your new Source Store
store_id_description: Description of your new Source Store
store_id_label: Visible label of selected Source Store on Hubspot object

pipeline_id: leave this property blank, when using the collection runner a script will check for an existing Ecommerce Pipeline, if present the pipeline id will be saved here, if not the next request will create the pipline and save the id here

create_pipeline_flag: set to true if you would like to create pipeline using collection runner
create_properties_flag: set to true if you would like to create properties using collection runner
create_example_objects_flag: set to true if you would like to create example objects using collection runner

created_contact_id: leave blank, used for object creation and associations
created_deal_id: leave blank, used for object creation and associations
created_product_id: leave blank, used for object creation and associations
created_line_item_id: leave blank, used for object creation and associations

ecommerce_property_group_internal_name: internal name of Ecommerce property group for each object
ecommerce_property_group_label: label of Ecommerce property group for each object

Open Collection runner:
Run all requests in collection
This will setup pipeline, create properties, and create example objects with associations.



