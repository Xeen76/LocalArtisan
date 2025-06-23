# Local Artisan Store - PHP Shopping Cart

A simple PHP-based shopping cart web application for a local artisan store. This project allows users to browse products, add them to a cart, and complete a checkout process. It uses PHP, MySQL, and Bootstrap for styling.

## Features
- Browse products with images and descriptions
- Add products to a shopping cart
- Update quantities or remove items from the cart
- Checkout with user details (name, email, address, etc.)
- Order summary and confirmation
- Responsive UI with Bootstrap

## Screenshots
Screenshots of the application can be found in the `ScreenShots/` directory:
- `scrnshot_1.png` - Home/Product listing page
- `scrnshot_2.png` - Product details page
- `scrnshot_3.png` - Cart view
- `scrnshot_4.png` - Checkout/Order confirmation

## Getting Started

### Prerequisites
- PHP 5.4+ (with mysqli extension)
- MySQL Server
- Web server (e.g., Apache)

### Installation
1. **Clone or Download the Repository**
   ```
   git clone <repo-url>
   ```
2. **Database Setup**
   - Import the SQL file `db/db_shopping_cart.sql` into your MySQL server. This will create the required database and tables, and insert sample products.
   - Example using phpMyAdmin or MySQL CLI:
     ```
     mysql -u root -p < db/db_shopping_cart.sql
     ```
3. **Configure Database Connection**
   - Edit `config.php` if your MySQL credentials differ from the default (`root`/no password).

4. **Place Images**
   - Product images are stored in the `images/` directory. Ensure the images referenced in the database exist in this folder.

5. **Run the Application**
   - Place the project folder in your web server's root directory (e.g., `htdocs` for XAMPP).
   - Access the app via `http://localhost/LocalArtisan-main/index.php`

## File Structure
- `index.php` - Product listing (home page)
- `view_details.php` - Product details and add to cart
- `view_cart.php` - View and update cart
- `checkout.php` - Enter delivery details and place order
- `complete.php` - Order confirmation
- `cart.class.php` - Cart management class
- `config.php` - Database connection
- `db/db_shopping_cart.sql` - Database schema and sample data
- `images/` - Product images
- `ScreenShots/` - Application screenshots

## Database Schema
The database includes the following tables:
- `products` (PID, PRODUCT, PRICE, IMAGE, DESCRIPTION)
- `users` (UID, NAME, CONTACT, ADDRESS, CITY, PINCODE, EMAIL)
- `orders` (OID, ORDER_NO, ORDER_DATE, UID, TOTAL_AMT)
- `order_details` (ID, OID, PID, PNAME, PRICE, QTY, TOTAL)

See `db/db_shopping_cart.sql` for full schema and sample data.

![image](https://github.com/user-attachments/assets/e41d8aae-5f28-4d86-b1d7-a6e4c5061c7d)


