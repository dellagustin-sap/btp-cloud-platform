<!-- loio2d758f7acc064e3c90a0b3a4fa907874 -->

# Defining Permitted Activities in an Authorization Object

To define the permitted activities for a service, create an authorization object with the standard authorization field *Activity* \(`ACTVT`\) for the permitted activities.



## Procedure

Follow the procedure in the ABAP development guide: [Defining an Authorization Object](https://help.sap.com/viewer/5371047f1273405bb46725a417f95433/Cloud/en-US/6135edd0bf75427fa932875a6e3b0378.html).

 > ### Note:  
> In our example, in the newly created authorization object, under *Authorization Fields*, you only need the predefined *Activity* authorization field to define the permitted activities for the business users of your service. In our example, these activities would be *01 Add or Create*, *02 Change*, *03 Display*, and *06 Delete* for standard activities.In addition, you need *93 Calculate* for the business object-specific activity *Calculate Bonus*. If you click on an empty row and choose [ENTER\], the list of available values is shown.
> 
> In theory, by using the syntax ***authorization: update*** on an operation in the entity's behavior definition, you could use the authorization check that is implemented for the update operation for the annotated operation. This is also referred to as “authorization delegation”. However, for security reasons, we recommend that you carefully consider whether you want to use authorization delegation because in this case, a user who is allowed to update a business object is then also allowed to perform all other activities on the business object.

 

<a name="loio2d758f7acc064e3c90a0b3a4fa907874__result_ask_l2j_vlb"/>

## Results

In the following, the newly created authorization object for the bonus calculation example is called `ZBNSCLC_AO`.

