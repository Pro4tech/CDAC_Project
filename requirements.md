# Requirement Set

1) For Guest (Done By Saurbh)
-View Property
-search Filters
 a)Category-vise -> eg:2BK,3BHK,Duplex,Bunglow
 b)location vise 
 	-> eg:Urban,Rural
 	-> eg:Hinjewadi [Optional as need APIs Data]
 c)Price-range (Optional)
 
2)For Registered User - **Buyer** (Done By Saurbh)
- View Property
- search Filters
 a)Category-vise -> eg:2BK,3BHK,Duplex,Bunglow
 b)location vise 
 	-> eg:Urban,Rural
 	-> eg:Hinjewadi [Optional as need APIs Data]
 c)Price-range (Optional)
- Purchase Property
	->Proceed with Payment
- Wishlist Property

3)For Registered User - Owner (Done By Pritesh)
- Add/Modify Property (Add,Delete,Change Property Details ie Sold or Available)
- List Properties Owned
- View Interested Buyers
- Owner has Option to show it's Contact Details with particular Linked Property 


4)System Functionalities (Done By Gaurav)
- Cart Functionalty
- Connectivity Between Owner and Buyer
 -> Mail or Contact Number
 -> Chat Bot Functionalities (Optional)
 
# Database
## Tables:
 1) Sites - with logging
 2) User - with logging
 3) Photos
 4) --City Validation Table-- [Containing City Names] 
 	->Inter-realated with State and Country Table
 
 
 
 Sites Table{
 	id - primary key auto increment
 	name
 	Description
 	price
 	location
 	Photos - foreign Key to photos tables
 	owner_id - foreign key to user tables
 	**logs****
 	
 }
 
 Photos Table{
 	id - primary key auto increment
 	site_id - foreign key to site 
 	link_image (href links)
 	attribute (description of Image eg Hall,Bedroom etc)
	 		
 }
 
 User Table{
 	id - primary key auto increment
 	name varchar(50)
 	profile_pic (Single href Link)	
 	email
 	contact_no
 	password (encrypted)
 	
} 
 City Table{
 	id - primary key auto increment
 	name varchar(50)
 	state_id
 	country_id
 
}
 State Table{
 	id - primary key auto increment
 	name
 	country_id

}
Country Table{
 	id - primary key auto increment
 	name
 	
} 	
 	
