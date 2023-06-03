---
id: "Fashion Cloud"
aliases:
  - "Fashion Cloud"
tags: []
---

# Fashion Cloud

## Home assessment
### Code
Search Result Page (SRP)

Product properties:
- GTIN -> unique id 13 digit ( number )
- Name (string)
- Image -> url (string) 
- Category -> enum (string)
- Stock (number)
- Price -> in euro (float)
- Brand name (string)

Non-Functional Requirements:
- Simple and clean UI
- Functionality
- Efficiency
- Code Structure
- Commit with good messages and sensible chunks
- Test the code
- Backend
	- Node.js v18
	- Typescript
	- MongoDB
	- Handle 20 million products in the db
- Frontend
	- Angular 14

Functional Requirements:
- [ ] See products list
- [x] Filters products by:
	- [x] Brand
	- [x] Category
- [x] Sorting
	- [x] Default sorting should be highest stock
- [ ] Select filter and sorting criteria from drop-down menus


Steps to do the app:
- Setup both projects
- Make backend GET api
- Add sorting
- Add filter
- Define tests
	- Test all sorting and filtering cases
	- Simple GET
	- Handle error case
- Define components frontend
	- dropdown
	- card
	- grid
	- **loader state**
- Define tests
	- e2e to check the filters and sorting api call
	- check that the ui updates
	- loader state

 - Backend todo list
	 - [x] Make product controller
	 - [x] Make product route
	 - [x] Add index router with product
	 - [x] fetch data from mongo
	 - [x] Add zod validation for sort
	 - [x] Zod validation filtering
	 - [x] Zod validation pagination
	 - [ ] Handle errors on controller
	 - [ ] make test cases
		 - [ ] simple case
		 - [ ] filter cases
		 - [ ] error case
		 - [ ] sorting case
		 - [ ] pagination case
   
### Think
Given this two collections
```
Product 
{
 ean: string;
 brandId: string;
 articleNumber: string;
 description: string;
 size: string;
 color: string;
}

PurchaseOrder 
{
 id: string;
 retailerId: string;
 ean: string;
 quantity: number;
 purchaseDate: Date;
}
```

Make a flowchart where we will fetch the 3 most popular colors per year

Result interface
```
[{
	year: number;
	popularColors: [{
		color: string,
		numberOfPurchase: number
	}]
}]
```

Use [app diagrams](https://app.diagrams.net/)

### Architect

### Notes
- The backend repo is missing this dependencies:
	- mongodb
 - backend is missing the .gitignore
 - backend has a bad model on brandName
- double check repo before adding fashion reviewer
