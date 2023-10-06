<h1 align="center">E-commerce Admin</h1>


<div align="center">
  
  ![Capa (2)](https://github.com/room-organization/ecommerce-admin/assets/98264322/3fcb5074-847c-41d7-a63d-8842bc0cee69)  
  
</div>

## Fetures
- This admin dashboard is going to serve as both CMS, Admin and API!
- The user will be able to control mulitple vendors / stores through this single CMS! (For example the user can have a "Shoe store" and a "Laptop store" and a "Suit store", and our CMS will generate API routes for all of those individually!)
- The user will be able to create, update and delete categories!
- The user will be able to create, update and delete products!
- You will be able to upload multiple images for products, and change them whenever you want!
- The user will be able to create, update and delete filters such as "Color" and "Size", and then match them in the "Product" creation form.
- The user will be able to create, update and delete "Billboards" which are these big texts on top of the page. You will be able to attach them to a single category, or use them standalone (Our Admin generates API for all of those cases!)
- The user will be able to Search through all categories, products, sizes, colors, billboards with included pagination!
- The user will be able to control which products are "featured" so they show on the homepage!
- The user will be able to see your orders, sales, etc.
- The user will be able to see graphs of your revenue etc.
- The user will learn Clerk Authentication!
- Order creation
- Stripe checkout
- Stripe webhooks



## Technologies

To build this project we are using the following technologies:

- <span>[**React.js**](https://react.dev/)</span>
- <span>[**Next.js**](https://nextjs.org/docs)</span>
- <span>[**Shadcn UI**](https://ui.shadcn.com/)</span>
- <span>[**Tailwind CSS**](https://tailwindcss.com/)</span>
- <span>[**TypeScript**](https://www.typescriptlang.org/)</span>
- <span>[**Clerck**](https://clerk.com/docs/quickstarts/nextjs)</span>
- <span>[**Cloudinary**](https://cloudinary.com/)</span>
- <span>[**Prisma**](https://www.prisma.io/) </span>
- <span>[**MySQL**](https://www.mysql.com/) </span>
- <span>[**Planet Scale**](https://planetscale.com/) </span>
- <span>[**Stripe**](https://stripe.com/) </span>

## Getting Started
### Prerequisites
To get started you must have the following softwares installed:
- <a href="https://nodejs.org/en/"> Node.js </a>
- <a href="https://git-scm.com/downloads"> git </a>
- <a href="https://www.docker.com/"> Docker </a>

### Instalation 

Open a terminal follow the steps bellow

1. Clone the repository: 

``` bash 
 $ git clone https://github.com/room-organization/ecommerce-admin.git
```

- Got to the project directory 
``` bash 
2. cd ecommerce-admin
```

3. Install depedencies

``` bash 
npm install
```
4. Execute Docker Compose

``` bash 
docker compose up
```

5. Setup .env file


```js
# CLerk
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=
NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL=/
NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL=/

# Prisma
DATABASE_URL=''

# Cloudinary
NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME=""

#  Stripe
STRIPE_API_KEY=
STRIPE_WEBHOOK_SECRET=

#  Frontend strore
FRONTEND_STORE_URL=http://localhost:3001

```

### Connect to PlanetScale and Push Prisma
```shell
npx prisma generate
npx prisma db push
```
Note: You need to run Docker compose only if you want to create a local database. Otherwise, you need to create a database in Planete Scale and set the DATBASE_URL with the connection string that Planete Scale will provide you.
If you want to create a local database you can set the DATABASE_URL as shown bellow and the run `docker compose` command:
```shell
DATABASE_URL="mysql://root:root@localhost:3306/<YourDatabaseName>"
```


6. Start the app

```shell
npm run dev
```

## API Routes for client side

```js
# Prouducts routes

$ GET /products
$ GET /products/id


# Billboard Rouetes

$ GET /billboards
$ GET /billboards/id

# Categories routes

$ GET /categories
$ GET /categories/id


# Sizes routes

$ GET /sizes
$ GET /sizes/id


#  Colors routes

$ GET /colors
$ GET /colors/id

#  Checkout

$ POST /checkout
```

## Contributing

Follow these steps to make your contribution.

### Create a new branch 

1. Create a new branch for your changes. The branch name should start with one of the following prefixes, depending on the type of changes you are making:
    - <strong>feat/</strong> for new features
    - <strong>fix/</strong> for bug fixes
    - <strong>docs/</strong> for documentation changes
    - <strong>style/</strong> for changes that do not affect the meaning of the code (e.g. formatting)
    - <strong>refactor/</strong> for code changes that neither fix a bug nor add a feature
2. Make your changes and commit them using Conventional Commits.
3. Push your changes to your feature branch.
4. Create a pull request.


### Convetional commits
We use Conventional Commits to standardize our commit messages. Please follow the guidelines below when making your commits:

1. Use the following format for your commit messages: `<type>(<scope>): <subject>`.
2. The <type> must be one of the following:
    - <strong>feat</strong>: a new feature
    - <strong>fix</strong>: a bug fix
    - <strong>docs</strong>: documentation changes
    - <strong>style</strong>: changes that do not affect the meaning of the code (e.g. formatting)
    - <strong>refactor</strong>: code changes that neither fix a bug nor add a feature
    - <strong>perf</strong>: code changes that improve performance
    - <strong>test</strong>: adding missing tests or correcting existing tests
3. The `<scope>` is optional and should be used to specify which part of the project your commit affects.
4. The `<subject>` should be a short description of the change.

Your contributions are valuable to us and we appreciate your efforts to make this project better.


Happy contributing ;)


