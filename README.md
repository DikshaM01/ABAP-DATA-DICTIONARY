# ABAP-DATA-DICTIONARY
THIS IS ABOUT SAP FIRST LESSION THAT IS DATA DICTIONARY SE11
data dictionary
-> data dictionary is used to create and manage the data. here we can create the table, insert the data, modify the data,it is the central repository , any modifications made to its data definations will be reflected in programs automatically.
-> using f1 help we can see about that keyword in the documentation which will be official.
-> using f4 help we can see all the possible suggestions of the input.
*************database tables******************
1. database tables are the most important part of the abap data dictionary.
2. here we define the tables independentaly which means that we are not writing in commands for example like sql to create the table in the database.
3. once the table is created the system by default will create the same structure of the table in the database which is known as transparent table. a transaprent table in a abap data dictionary has a one to one projection of the database. when we define a transparent table in abap data dictionary, exactly one database table with identical names and feilds in created in the database.
4. if you want to change the type of the table to other table you can do by going to the extra then change the table type mode.
5. there are other types of tables other then transparent table that is pooled table and cluster table.
6. the transparent table will have one to one relationship with the database while other two tables are having one to many relationship with the database.
*****************creating the database table******************
   1. on the initial screen of the abap dictionary select the database radio button, enter the name of the database table you wish to create and click on the create button. the name should be start with zdt.
   2. then you have to write about the description of the table.
   3. next change table view will open there you have to select delivery class and    table view maintenance.
   4. delivery class- this will define which type of  data the database will contain. it will also control the transport of the table data during the upgradation,installations, upgrades and client copies.
   5. table view maintenance-> this field allows to restrict whether the data can be entered manually, who will be viewing the data and maintaining the data.
   6. the authorization group in the technical settings will decide who will be having the access to the data.
   7. once the settings in the delivery and maintenance tab is maintained,
   8. click on the field tab where you will maintain the field which should not be longer then the 16 character.
   9. key-> if you will click on the key the data in this will be unique and not null.
   10. initial -> if clicking on this then the feild be not null, by default it will take the default type of the data type or initial values for all the rows.
   11. data element-> data element will define the technical and semantic attributes. the technical attributes will include data type, length,decimal places and short description.
   12. here if you click on the predefined tab then you will manually enter the type of the data, length of the data and description of the data.
   13. in data element you can give the fixed values, value range, intervals in the domain
   14. once you have done with the entries in the fields tab go to the entry help/check tab and if any input help or search help is there then it will be present there.
   15. if the table has fields of type currency or quantity  type then the refrence fields should be maintained in the currency/quantity feilds tab.
   16. currency fields-> cuky and quantity fields ->unit
   17. once all the feilds are maintained then you have to maintain the enhancement category in extras.
   18. can be enhanced->select this option if the table can be enhanced by adding fields of any type
   19. can be enhanced(character type or numeric)-> select this option if the table can be enhanced with the character or numeric fields.
   20. can be enhanced(character) enhanced with character type fields-> c,n,d,t,x
   21. cannot be enhanced-> if table will not be enhanced in any way.
   22. enhancement category will work like while adding structure
   23. once enhancement categpry is maintained , you need to maintain the technical setting of the table
   24. technical settings will define how the table is created in the database.
   25. data class -> this will decide the physical area of the database in which table is created. master data, transaction data , customized data.
   26. size category-> size category determines the initial memory space to be allocated for the database table, if the initiak memory space is used up, the size of the table will be incremented by the same value known as extends.
   27. buffering-> these settings determine whether the data in the database table will be buffered or not. if the buffering is switched on then the system will keep the copy of the database content in the application server to speed up the data selection and improve performance.
   28. buffering is not allowed for the transaction data because it will be changed frequently.
   29. buffering  not allowed-> this settings turns off the buffering for the database tables , buffering allowed but switched off->now the buffered is switched off for the database table when delivered but can be activated in later system depending on how the table is used, buffering activated-> the data will be saved or if any changes will happen then it will also get saved.
   30. buffering type-> if the table buffer is activated then buffering types must be defined.
   31. single records buffered-> select only those rows that are accessed by the program are buffered,if generic area buffered is selected the number of key fields should be entered in the input fields, when the database table is read then the data related to the database table the system will give all the matching records, if fully buffered is selected all the rows are buffered when a row of the table is read.
   32. indexes-> we use both primary index and secondary index
   33. primary index -> by default it will be created,when the database table is created, the system generates the primary index  for the key fields. the entries in the index are always sorted to provide faster access to the table records.
   34. secondary index , if in the where clause we are not using the key fields then we are creating the secondary index of non primary key field.
   35. change index screen provide a meaningful short description . on this you have the option to select to create a unique index or a non unique index. if the values of the index field uniquely identifies the row then unique, when you select the non unique index you can also select if the index should be created in all the database systems or not created at all in the database.
       ******************table maintenance generator******************
       1. to make it easy for users to input data into a database table, we can generate maintenance view for the database table.
       2. for that select the delivery maintenance tab select delivery/maintenace allowed from the dropdown and activate the table.
       3. authorization group-> provide the authorization group to restrict the maintenance permission to select users. enter &nc& in this field if you dont want to set any restrictions.
       4. function group -> enter the name of the function group in which all the required code will be generated.
       5. package-> displays the package in which object is assigned.
       6. maintenace type->one step-> this will create the single screen for displays and maintenanec
       7. two step-> this will create two screen one for display and other for maintenance.
       
