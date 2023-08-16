# Ada - Santander Coders: Unit 02

### Contacts App Project

This project is a contacts app software that allows users to create, edit, delete and search contacts.

- [Statement](#statement)
- [Concepts](#concepts)

[See the project in Development Environment](https://github.dev/arthurbicego/ada-santander-coders-02/)

---

### Statement

Using object-oriented concepts, create a contact app system.
- The app must allow storing multiple contacts, containing at least first and last name information.
- A contact can have multiple phones.
- A contact can have multiple addresses.
- The storage of phones must allow the inclusion of area code and number information separately.
- The storage of addresses must allow the inclusion of zip code, address, number, city and state information separately.
- The system should allow interaction with the user with the following actions:

```
- Add a contact and their data;
- List all contacts in the phonebook;
- Search for a contact according to a keyword (Use first name, last name data to perform the search)
- Remove a contact from the phonebook;
- Remove all contacts from the phonebook;
- Add a phone to a contact;
- Add an address to a contact;
- Remove a phone number from a contact in the phonebook;
- Remove an address of a contact from the phonebook;
- View all contact information from the phonebook;
- List all phone numbers of a contact in the phonebook;
- List all addresses of a contact in the phonebook;
- View all phone information of a phonebook contact;
- View all address information for a contact in the phonebook;
```

Additional actions that can be included in the Agenda as a bonus:

```
- Display contact list with pagination. Including the option to navigate to the next or previous page;
- View the contact's phone list with paging. Including the option to navigate to the next or previous page;
- Display contact address list with pagination. Including the option to navigate to the next or previous page;
- Export all contacts to a text file;
- Import all contacts from a text file;
- Automatically load and save all contacts to a text file. Making the agenda a 100% functional program;
```

---

### Some Concepts

<details>
  <summary>Casting</summary>

  ```java
split[2] = String.valueOf(Integer.parseInt(split[2]) - quantity);
  ```
</details>
<details>
  <summary>Input</summary>

  ```java
String id = scanner.nextLine();
  ```
</details>
<details>
  <summary>Output</summary>

  ```java
System.out.println("Are you sure you want to " + method + " Product " + id + "?");
  ```

  ```java
System.out.printf("The total checkout amount is: $%.2f", checkoutValue);
System.out.println();
  ```
</details>

<details>
  <summary>Array and String</summary>

  ```java
String[] split = productLine.split("\\|");
  ```

  ```java
split[1].toUpperCase().contains(name.toUpperCase())
  ```

  ```java
Objects.equals(split[0], id)
  ```
</details>
<details>
  <summary>Logical Operator</summary>

  ```java
productLine != null
  ```
</details>
<details>
  <summary>Selection Statement</summary>

  ```java
if (size == 0) {
    product.setId("0");
} else {
    List<String> products = Files.readAllLines(path);
    size--;
    String[] split = products.get(size).split("\\|");
    Integer valueOf = Integer.valueOf(split[0]);
    valueOf++;
    product.setId(String.valueOf(valueOf));
}
  ```
</details>
<details>
  <summary>Enhanced Switch</summary>

  ```java
switch (choice) {
    case "1" -> {
        groceryController.listProducts();
    }
  ```
</details>
<details>
  <summary>For, Enhanced For, ForEach</summary>

  ```java
for (int i = 0; i < cartProducts.size(); i++) {
    if (Objects.equals(cartProducts.get(i).getId(), id)) {
        cartProducts.remove(i);
        cart.setProductsCart(cartProducts);
    }
}
  ```
  ```java
for (Product product : products) {
    checkoutValue = checkoutValue + (product.getQuantity() * product.getPrice());
}
  ```
  ```java
products.forEach(product -> GroceryView.showProduct(product))
  ```
</details>
<details>
  <summary>Exceptions</summary>

  ```java
try {
    quantity = scanner.nextInt();
    scanner.nextLine();
} catch (Exception e) {
    System.out.println();
    System.out.println("Error registering the quantity. Default quantity (1) has been set.");
    quantity = 1;
}
  ```
</details>
<details>
  <summary>File Handling</summary>

  ```java
Path path = Paths.get("src/tech/ada/products.txt")
  ```
  ```java
Files.readAllLines(path);
  ```
  ```java
Files.write(path, products);
  ```
</details>
