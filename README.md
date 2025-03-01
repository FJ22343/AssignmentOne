class Customer:
    """Represents a customer in the delivery system."""

    def __init__(self, customer_id, name, address, phone_number, email, order_history=None):
        """Constructor for Customer class."""
        self._customer_id = customer_id
        self._name = name
        self._address = address
        self._phone_number = phone_number
        self._email = email
        self._order_history = order_history or []  # List of order IDs

    # Getters
    def get_customer_id(self):
        return self._customer_id

    def get_name(self):
        return self._name

    def get_address(self):
        return self._address

    def get_phone_number(self):
        return self._phone_number

    def get_email(self):
        return self._email

    def get_order_history(self):
        return self._order_history

    # Setters
    def set_name(self, name):
        self._name = name

    def set_address(self, address):
        self._address = address

    def set_phone_number(self, phone_number):
        self._phone_number = phone_number

    def set_email(self, email):
        self._email = email

    def add_order(self, order_id):
        """Adds an order ID to the customer's order history."""
        self._order_history.append(order_id)

    def place_order(self):
        """Simulates placing an order (implementation to be added)."""
        pass

    def process_payment(self):
        """Simulates processing a payment (implementation to be added)."""
        pass


class Driver:
    """Represents a driver in the delivery system."""

    def __init__(self, driver_id, name, license_number, vehicle_type, phone_number, current_delivery=None):
        """Constructor for Driver class."""
        self._driver_id = driver_id
        self._name = name
        self._license_number = license_number
        self._vehicle_type = vehicle_type
        self._phone_number = phone_number
        self._current_delivery = current_delivery  # Delivery ID

    # Getters
    def get_driver_id(self):
        return self._driver_id

    def get_name(self):
        return self._name

    def get_license_number(self):
        return self._license_number

    def get_vehicle_type(self):
        return self._vehicle_type

    def get_phone_number(self):
        return self._phone_number

    def get_current_delivery(self):
        return self._current_delivery

    # Setters
    def set_name(self, name):
        self._name = name

    def set_license_number(self, license_number):
        self._license_number = license_number

    def set_vehicle_type(self, vehicle_type):
        self._vehicle_type = vehicle_type

    def set_phone_number(self, phone_number):
        self._phone_number = phone_number

    def set_current_delivery(self, delivery_id):
        self._current_delivery = delivery_id

    def view_delivery_assignments(self):
        """Simulates viewing delivery assignments (implementation to be added)."""
        pass

    def update_delivery_status(self):
        """Simulates updating the delivery status (implementation to be added)."""
        pass

    def schedule_delivery(self):
        """Simulates scheduling a delivery (implementation to be added)."""
        pass


class SystemAdministrator:
    """Represents a system administrator in the delivery system."""

    def __init__(self, admin_id, name, email, phone_number, role, managed_drivers=None):
        """Constructor for SystemAdministrator class."""
        self._admin_id = admin_id
        self._name = name
        self._email = email
        self._phone_number = phone_number
        self._role = role
        self._managed_drivers = managed_drivers or []  # List of driver IDs

    # Getters
    def get_admin_id(self):
        return self._admin_id

    def get_name(self):
        return self._name

    def get_email(self):
        return self._email

    def get_phone_number(self):
        return self._phone_number

    def get_role(self):
        return self._role

    def get_managed_drivers(self):
        return self._managed_drivers

    # Setters
    def set_name(self, name):
        self._name = name

    def set_email(self, email):
        self._email = email

    def set_phone_number(self, phone_number):
        self._phone_number = phone_number

    def add_managed_driver(self, driver_id):
        """Adds a driver ID to the list of managed drivers."""
        self._managed_drivers.append(driver_id)

    def manage_drivers(self):
        """Simulates managing drivers (implementation to be added)."""
        pass

    def send_notifications(self):
        """Simulates sending notifications (implementation to be added)."""
        pass


class Order:
    """Represents an order in the delivery system."""

    def __init__(self, order_id, customer_id, order_date, items, total_amount, delivery_address, delivery_status="Pending"):
        """Constructor for Order class."""
        self._order_id = order_id
        self._customer_id = customer_id
        self._order_date = order_date
        self._items = items  # List of item IDs or item objects
        self._total_amount = total_amount
        self._delivery_address = delivery_address
        self._delivery_status = delivery_status

    # Getters
    def get_order_id(self):
        return self._order_id

    def get_customer_id(self):
        return self._customer_id

    def get_order_date(self):
        return self._order_date

    def get_items(self):
        return self._items

    def get_total_amount(self):
        return self._total_amount

    def get_delivery_address(self):
        return self._delivery_address

    def get_delivery_status(self):
        return self._delivery_status

    # Setters
    def set_delivery_status(self, status):
        self._delivery_status = status

    def add_item(self, item_id):
        """Adds an item ID to the order."""
        self._items.append(item_id)

    def calculate_total_amount(self):
        """Simulates calculating the total amount of the order (implementation to be added)."""
        pass


class Delivery:
    """Represents a delivery in the delivery system."""

    def __init__(self, delivery_id, order_id, driver_id, delivery_date, delivery_time, delivery_address, delivery_status="Scheduled"):
        """Constructor for Delivery class."""
        self._delivery_id = delivery_id
        self._order_id = order_id
        self._driver_id = driver_id
        self._delivery_date = delivery_date
        self._delivery_time = delivery_time
        self._delivery_address = delivery_address
        self._delivery_status = delivery_status

    # Getters
    def get_delivery_id(self):
        return self._delivery_id

    def get_order_id(self):
        return self._order_id

    def get_driver_id(self):
        return self._driver_id

    def get_delivery_date(self):
        return self._delivery_date

    def get_delivery_time(self):
        return self._delivery_time

    def get_delivery_address(self):
        return self._delivery_



        #4


        # Create Customer object
customer = Customer(
    customer_id="CUST123",
    name="Sarah Johnson",
    address="45 Knowledge Avenue, Dubai, UAE",
    phone_number="123-456-7890",
    email="sarah.johnson@example.com"
)

# Create Driver object
driver = Driver(
    driver_id="DRIVER456",
    name="John Smith",
    license_number="DL1234567890",
    vehicle_type="Van",
    phone_number="987-654-3210"
)

# Create SystemAdministrator object
admin = SystemAdministrator(
    admin_id="ADMIN789",
    name="Jane Doe",
    email="jane.doe@example.com",
    phone_number="555-123-4567",
    role="Senior Admin"
)

# Create Order object
order = Order(
    order_id="DEL123456789",
    customer_id=customer.get_customer_id(),
    order_date="January 25, 2025",
    items=[
        {"item_code": "KB123", "description": "Wireless Keyboard", "quantity": 1, "unit_price": 75.00},
        {"item_code": "MS456", "description": "Wireless Mouse & Pad Set", "quantity": 1, "unit_price": 120.00},
        {"item_code": "CP789", "description": "Laptop Cooling Pad", "quantity": 1, "unit_price": 50.00},
        {"item_code": "CL012", "description": "Camera Lock", "quantity": 1, "unit_price": 25.00}
    ],
    total_amount=270.00,
    delivery_address=customer.get_address()
)

# Create Delivery object
delivery = Delivery(
    delivery_id="DN-2025-001",
    order_id=order.get_order_id(),
    driver_id=driver.get_driver_id(),
    delivery_date="January 25, 2025",
    delivery_time="10:00 AM",
    delivery_address=customer.get_address()
)

# (Note: Payment class is not used here since the diagram doesn't provide enough details)

# Display Delivery Note
print("Delivery Note\n")
print("Thank you for your order!\n")
print("Recipient Details:")
print(f"Name: {customer.get_name()}")
print(f"Contact: {customer.get_email()}")
print(f"Delivery Address: {customer.get_address()}\n")
print("Delivery Information:")
print(f"Order Number: {order.get_order_id()}")
print(f"Reference Number: {delivery.get_delivery_id()}")
print(f"Delivery Date: {delivery.get_delivery_date()}")
print(f"Delivery Method: Courier")  # Assuming delivery method
print(f"Total Weight: 7 kg\n")  # Assuming total weight
print("Summary of Items Delivered:")
print("{:<15} {:<30} {:<10} {:<15} {:<15}".format("Item Code", "Description", "Quantity", "Unit Price (AED)", "Total Price (AED)"))
for item in order.get_items():
    total_price = item['quantity'] * item['unit_price']
    print("{:<15} {:<30} {:<10} {:<15} {:<15}".format(item['item_code'], item['description'], item['quantity'], item['unit_price'], total_price))
print(f"\nSubtotal: AED {order.get_total_amount():.2f}")
print(f"Taxes and Fees: AED 13.50")  # Assuming taxes and fees
print(f"Total Charges: AED 283.50")  # Assuming total charges
