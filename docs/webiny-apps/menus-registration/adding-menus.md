---
id: adding-menus
title: Adding menus
sidebar_label: Adding menus
---

## Menu setup

One of the main sections of the Admin app is the main menu, which is located on the left side of the screen.

![Menu example](/img/webiny-apps/menu-registration/menu-example.png)

To add a new menu you will need to register it as a plugin.

The following snippet of code shows how to add a new menu via a simple plugin:

```javascript
  {
    type: "menu",
    name: "ecommerce",
    render({ Menu, Section, Item }) {
      return (
        <Menu name="shop" label={"Shop"}>
          <Section label={"Products"}>
            <Item label={"Products"} path="/shop/products" />
            <Item label={"Manage stock"} path="/shop/stock" />
          </Section>
          <Section label={"Customers"}>
            <Item label={"Customers"} path="/shop/customers" />
            <Item label={"Discounts"} path="/shop/discounts" />
          </Section>
        </Menu>
      );
    }
  }
```
You can find out how to add a new route [here](/docs/webiny-apps/routes-registration/add-routes).

You should add code above to your plugins array as you can see in the example below.
```javascript
Use the provided Menu, Section, and Item components to organize the menus to the expected structure.
```

After doing these steps you should have your menu up when you rebuild your project.

![Menu Registration](/img/webiny-apps/menu-registration/new-menu-example.png)
