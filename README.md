# Food_ordering_app
```markdown
# Food Ordering App (Tkinter)

A simple desktop food ordering interface built with Python’s Tkinter library.  
Users can select items from a menu, add them to a cart, view the running total, and place an order.

---

## Features

- Graphical user interface (GUI) using Tkinter
- Predefined menu with item names and prices
- Add multiple quantities of the same item to the cart
- Cart display shows each item, quantity, and subtotal
- Automatic total calculation
- Order confirmation dialog
- Handles empty cart when trying to place an order

---

## Requirements

- Python 3.x  
- Tkinter (usually included by default with standard Python installations)

To check Tkinter availability:

```bash
python -m tkinter
```

If a small window appears, Tkinter is installed correctly.

---

## Installation & Running

1. Save the provided code into a file, for example:

   ```bash
   food_ordering_app.py
   ```

2. Run the script with Python:

   ```bash
   python food_ordering_app.py
   ```

A window titled **“Food Ordering App”** should open.

---

## How to Use

1. **Select an item**  
   Click an item in the *Menu* list (e.g., "Pizza").

2. **Add to Cart**  
   Click the **“Add to Cart”** button.  
   - A popup will confirm the item was added.  
   - The *Your Cart* text area updates with:
     - Item name
     - Quantity (e.g., `x2`)
     - Subtotal price for that item

3. **View Total**  
   At the bottom of the cart display, you’ll see:

   ```text
   Total: $XX.XX
   ```

4. **Place Order**  
   Click **“Place Order”**:
   - If the cart is empty, a warning appears.
   - If not empty, you’ll be asked to confirm the order.
   - On confirmation:
     - A “Thank you” message shows.
     - The cart is cleared and the display is reset.

---

## Code Overview

- `menu`: A dictionary containing item names and their prices.
- `cart`: A dictionary that tracks items and their quantities.

### Functions

- `add_to_cart()`
  - Gets the currently selected menu item.
  - Increments quantity in `cart`.
  - Calls `update_cart_display()`.
  - Shows a confirmation messagebox.

- `update_cart_display()`
  - Clears the cart text area.
  - Loops through `cart` items, calculating:
    - Subtotal per item (`price * quantity`)
    - Running total for the whole order
  - Displays all items and the total.

- `place_order()`
  - Checks if `cart` is empty.
  - If not, asks for confirmation.
  - On confirmation, shows success message, clears `cart`, and updates display.

---

## Customization

- **Change the Menu Items or Prices**

  Edit the `menu` dictionary at the top:

  ```python
  menu = {
      "Burger": 5.99,
      "Pizza": 8.99,
      "Salad": 4.49,
      "Fries": 2.99,
      "Soda": 1.99
  }
  ```

  Add, remove, or rename items, and adjust prices as needed.

- **Change Window Size or Title**

  ```python
  root.title("Food Ordering App")
  root.geometry("400x400")
  ```

  Modify these lines to set a different title or window dimensions.

---

## Notes

- This is a basic example intended to demonstrate Tkinter GUI concepts:
  - Listbox usage
  - Text widget for display
  - Message boxes for feedback
- It does not include payment processing, user accounts, or persistence (data is lost when the app is closed).
```
