---
name: Meta Data Object
---
## `metadata` Object

The `metadata` object allows you to include additional custom key-value pairs for advanced coupon validations. This provides flexibility in defining coupon applicability based on specific business requirements. The object can be passed within both the `order` and `items` objects.

| Parameter | Description                                                    | Required/Optional | Data Type | Sample Value |
| --------- | -------------------------------------------------------------- | ----------------- | --------- | :----------- |
| `key`     | Metadata property name (for example, color, size, supplier).   | Optional          | String    | `color`      |
| `value`   | Metadata property value (for example, Red, Large, Supplier A). | Optional          | String    | `red`        |

The `metadata` key-value pairs enhance the coupon validation logic by allowing custom attributes to be considered during the validation process. For example, a coupon could be applicable only for items of a specific color (Red) or size (Large) or a specific supplier (SupplierA). By including such metadata, the system validates the coupon based on these additional criteria, ensuring accurate coupon applicability.

> 📘 Recommendation
>
> CleverTap recommends passing the `order` and `items` object details when calling this API on the checkout page. This displays the right coupons to the users in the coupon tray.
