# Djangoinvoice11


Description
Django Invoice API is a web application that allows users
to manage invoices and their details. 
It provides APIs for creating, retrieving, updating, and deleting invoices.
The API accepts JSON payload for invoice data and supports nested serializers 
to handle invoice details.

Requirements:
Python (>= 3.6)
Django (>= 2.2)
Django REST framework (>= 3.12)

Installation:
Clone the repository:
git clone <repository_url>
cd DjangoInvoice

Set up a virtual environment (optional but recommended):
python -m venv venv
source venv/bin/activate    # On Windows, use `venv\Scripts\activate`

Run the development server:
python manage.py runserver

API Endpoints
GET /invoices/: Retrieve a list of all invoices.
POST /invoices/: Create a new invoice by providing the invoice data as JSON payload.
GET /invoices/<invoice_id>/: Retrieve details of a specific invoice.
PUT /invoices/<invoice_id>/: Update an existing invoice with new data.
DELETE /invoices/<invoice_id>/: Delete a specific invoice.


JSON Payload Format:
To create or update an invoice,
use the following JSON payload format:

{
    "date": "YYYY-MM-DD",
    "invoice_no": "INV-2023-001",
    "customer_name": "John Doe",
    "invoice_details": [
        {
            "description": "Item 1",
            "quantity": 2,
            "unit_price": 10.99
        },
        {
            "description": "Item 2",
            "quantity": 1,
            "unit_price": 5.50
        }
    ]
}

Testing
To run the test cases for the API endpoints, use the following command:
python manage.py test
