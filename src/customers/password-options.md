---
title: Password Options
---

The customer password options determine the level of security that is used for password reset requests, the email templates that are used for customer notification, and the lifetime of the password recovery link. You can allow customers to change their own passwords or require that only store administrators can do so

## To configure customer password options:

1. On the _Admin_ sidebar, go to **Stores** > _Settings_ > **Configuration**.

1. In the panel on the left, expand **Customers** and choose **Customer Configuration**.

1. Expand ![]({% link images/images/btn-expand.png %}){: .Inline} the **Password Options** section.

    ![]({% link images/images/config-customers-customer-configuration-password-options.png %}){: .zoom}
    [_Password Options_]({% link configuration/customers/customer-configuration.md %})

1. Set the **Password Reset Protection Type** to the method you want to use for managing password reset requests:

    | By IP and Email | The password can be reset online after a response is received from a reset notification sent to the email address associated with the Admin account. |
    | By IP | The password can be reset online without additional confirmation. |
    | By Email | The password can be reset only by responding to an email notification that is sent to the email address associated with the Admin account. |
    | None | The password can be reset only by the store administrator. |

1. To limit the number of password reset requests sent per hour, do the following:

    - In the **Max Number of Password Reset Requests** field, enter the maximum number of password reset requests that can be sent per hour.

    - In the **Min Time Between Password Reset Requests** field, enter the minimum number of minutes that must elapse between requests.

1. To configure the password reset email notification, do the following:

    - Set **Forgot Email Template** to the template that is used for the email sent to customers who have forgotten their passwords.

    - Set **Remind Email Template** to the template that is used when a password hint is sent to customers.

    - Set **Reset Password Template** to the template that is used when customers change their passwords.

    - Set **Password Template Email Sender** to the [store contact]({% link stores/store-email-addresses.md %}) that appears as the sender of password-related notifications.

1. Complete the following password reset security options:

    - In the **Recovery Link Expiration Period (hours)** field, enter the number of hours before the password recovery link expires.

    - In the **Number of Required Character Classes** field, enter the number of different character types that must be included in a password based on the following character classes:

      - Lowercase
      - Uppercase
      - Numeric
      - Special Characters

    - In the **Maximum Login  Failures to Lockout Account** field, enter the number of failed login attempts until the Admin account is locked. For unlimited attempts, enter zero (0).

    - In the **Minimum Password Length** field, enter the minimum number of characters that can be used in a password. The number must be greater than zero.

    - In the **Lockout Time (minutes)** field, enter the number of minutes an Admin account is locked after too many failed attempts to log in.

1. When complete, click <span class="btn">Save Config</span>.
