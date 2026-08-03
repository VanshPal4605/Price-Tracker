Smart Product Price Tracker
Overview
The Smart Product Price Tracker is an automated web application designed to help users save money by monitoring the cost of goods across major e-commerce platforms. Instead of manually checking websites for discounts, users can simply paste a product URL from sites like Amazon, Walmart, or Zara into their personal dashboard.

Once a product is added, the application takes over. It instantly extracts the product's name, current price, and image, saving it to a secure database. Every day, an automated background process revisits the product page to check for price changes. If the system detects that the price has dropped below the originally tracked amount, it immediately dispatches an email alert to the user, ensuring they never miss a deal.

Core Features
Universal Product Tracking: Capable of scraping and tracking product pages from almost any major online retailer without requiring site-specific code.

Interactive Price History: Visualizes the price fluctuations of tracked items over time using detailed, interactive charts.

Automated Daily Monitoring: Utilizes background cron jobs to check prices every single day without any user intervention required.

Instant Email Alerts: Automatically sends a notification straight to the user's inbox the moment a price drop is recorded.

Secure User Accounts: Keeps user data and tracked products strictly private using Google OAuth and database-level security policies.

Technology Stack
Frontend & User Interface
Next.js 16 (App Router): The core React framework used to build a fast, server-rendered, and SEO-friendly application structure.

Tailwind CSS & shadcn/ui: Provides a highly customizable, modern, and responsive user interface with pre-built, accessible components.

Recharts: A composable charting library used to render the interactive price history graphs on the user's dashboard.

Backend & Database
Supabase: An open-source Firebase alternative that powers the entire backend infrastructure.

PostgreSQL: The robust relational database storing user profiles, product details, and historical price data.

Row Level Security (RLS): Ensures strict data privacy so users can only view and modify the products they are personally tracking.

pg_cron: A database extension used to schedule and execute the automated daily price-checking routines.

Google OAuth: Handles secure user authentication and login sessions.

Data Extraction & Notifications
Firecrawl: An advanced web data extraction API. It is specifically used because it can handle dynamic JavaScript rendering, automatically bypass anti-bot protections, and utilize AI to extract structured product data reliably.

Resend: A modern transactional email API used to format and deliver the automated price drop alerts directly to the user's email address.

Built by Vansh Pal