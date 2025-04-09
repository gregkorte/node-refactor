# Building the First Version of the Bangazon Site

## Learning Objectives

* Pug templates
* ERD Development
* Sequelize DB Models
* Sequelize Migrations
* Authentication

## Requirements

You will be building an Express application that will be the first, stable version of the Bangazon Platform product site.

### Models

1. Products will be created by customers, so make sure that you have a column on the `Product` model to store which customer created it.
1. Add a new model named `ProductType`. Add a foreign key to `ProductType` in the `Product` model. It must be non-nullable. The only fields needed are the primary key, and `Label`.
1. Add a model named `PaymentType`.
1. A `Customer` can have many payment types.
1. The `Order` model must have a foreign key field to the `PaymentType` model, but it can be nullable. However, before an order can be completed, there must be a value for the `PaymentType` field.

### Generated Application
Make sure you produce a standard layout with your `index.html` Pug template for the application so that the structure of each page is consistent.

1. User registration and login.
1. Product creation form for user to sell a product.
1. List of all product types.
1. Provide a view to show all products that are of a particular product type.
1. List all products, with the name text as a hyperlink to the detail view.
1. Provide a product detail view.
1. List payment types for current customer.
1. On the product detail view, have an `Add to Order` button that, when clicked, either creates a new order for a customer that doesn't have an active one, or adds to an existing open order.
1. In the navigation bar, have an affordance that shows the current customer how many items are in their order.
1. If the user clicks on their order in the navigation bar, take them to the order detail view, which lists products, their prices, and current total for order.
1. On the order detail view, have a button labeled `Complete Order`.
1. When a customer starts to complete an order, show them a list of payment types that are assigned to them. When they select one to add to the order, then the order is complete.

## Resources

### Sequelize Models and Migrations
Using the requirements above use Sequelize to create a [model](http://docs.sequelizejs.com/manual/tutorial/models-definition.html) for each resource, and use [migrations](link to sqlize docs) to ensure your database structure is up to date. Remember to start with a `.sequelizerc` file, and to run `sequelize init` to generate the needed directories and files.
[Sequelize CLI docs](https://github.com/sequelize/cli)

### Templates

[Pug](https://pugjs.org/api/getting-started.html)