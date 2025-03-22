# STEEM Local HTML Js Tool

This repository contains two simple local web-based tools for interacting with the STEEM blockchain:
1. **STEEM Delegation Tool**: Allows users to delegate STEEM Power (VESTS) to another account.
2. **STEEM Cancel Delegation Tool**: Allows users to cancel an existing delegation by setting the delegated VESTS to zero.

Both tools are built using HTML, JavaScript, and the `steem-js` library.

---

## Features

### STEEM Delegation Tool
- Input your username, active key, delegatee username, and the amount of STEEM to delegate.
- Automatically converts STEEM to VESTS using the current blockchain conversion rate.
- Broadcasts the delegation transaction to the STEEM blockchain.
- 
![image](https://github.com/user-attachments/assets/a530529c-a686-4669-9c9a-933a7157e4d3)


### STEEM Cancel Delegation Tool
- Input your username, active key, and the delegatee username.
- Cancels all delegated VESTS by setting the delegation amount to `0.000000 VESTS`.
- Broadcasts the cancellation transaction to the STEEM blockchain.
- 
![image](https://github.com/user-attachments/assets/c1df38d7-cc1f-47ff-a731-7f4a3900f23a)

---

## Prerequisites

To use these tools, you need:
- Host the code locally on your desktop
- A modern web browser.
- A STEEM account with an active key.
- An internet connection to interact with the STEEM blockchain.

---

## Setup

1. Clone or download this repository to your local machine.
2. Open the `index.html` file for the **STEEM Delegation Tool** or the `cancel_delegation.html` file for the **STEEM Cancel Delegation Tool** in your web browser.
3. Ensure you have the `steem-js` library loaded (already included via CDN in the code).

---

## CDN Usage

The `steem-js` library is loaded via a CDN (Content Delivery Network) in the `<head>` section of the HTML files. This ensures that the library is always up-to-date and readily available without requiring local installation.

### CDN Link
The following CDN link is used to load the `steem-js` library:
```html
<script src="https://cdn.jsdelivr.net/npm/steem/dist/steem.min.js"></script>
```

## Usage

### STEEM Delegation Tool
1. Open the `index.html` file in your browser.
2. Fill in the form:
   - **Your Username**: Your STEEM account username.
   - **Your Active Key**: Your STEEM account's active private key.
   - **Delegatee Username**: The username of the account you want to delegate to.
   - **Amount of STEEM to Delegate**: The amount of STEEM you want to delegate.
3. Click the **Delegate STEEM** button.
4. Wait for the transaction to be broadcasted. You will receive a success or error message.

### STEEM Cancel Delegation Tool
1. Open the `cancel_delegation.html` file in your browser.
2. Fill in the form:
   - **Your Username**: Your STEEM account username.
   - **Your Active Key**: Your STEEM account's active private key.
   - **Delegated Username**: The username of the account you previously delegated to.
3. Click the **Cancel Delegation** button.
4. Wait for the transaction to be broadcasted. You will receive a success or error message.

---

## Monitoring Operations in the Browser Console

To debug or monitor the operations, you can use the browser's developer console. Here's how:

### Opening the Console
- **Chrome/Firefox/Edge**: Press `F12` or `Ctrl + Shift + I` (Windows/Linux) or `Cmd + Option + I` (Mac) to open the developer tools. Navigate to the **Console** tab.
- **Safari**: Enable the developer menu by going to `Preferences > Advanced > Show Develop menu in menu bar`. Then, press `Cmd + Option + I` to open the developer tools and navigate to the **Console** tab.

### What to Look For
- **STEEM Delegation Tool**:
  - The console will log the calculated VESTS amount and the constructed delegation operation.
  - If the transaction is successful, you will see a log like: `Delegation successful: [transaction details]`.
  - If there’s an error, the console will display the error message for debugging.
- **STEEM Cancel Delegation Tool**:
  - The console will log the constructed cancellation operation.
  - If the transaction is successful, you will see a log like: `Cancel delegation successful: [transaction details]`.
  - If there’s an error, the console will display the error message for debugging.


---

## Security Notes
- **Never share your active key**: Your active key grants full access to your STEEM account. Only use it in trusted environments.
- **Use locally**: For maximum security, run these tools locally on your machine and avoid sharing your active key online.
- **Double-check inputs**: Ensure all form inputs are correct before submitting the transaction.

---

## Code Overview

### STEEM Delegation Tool
- The tool calculates the equivalent VESTS for the entered STEEM amount using the current blockchain conversion rate.
- It constructs a `delegate_vesting_shares` operation and broadcasts it to the STEEM blockchain.

### STEEM Cancel Delegation Tool
- The tool constructs a `delegate_vesting_shares` operation with `0.000000 VESTS` to cancel all delegated VESTS.
- It broadcasts the operation to the STEEM blockchain.

---

## Dependencies
- [steem-js](https://github.com/steemit/steem-js): A JavaScript library for interacting with the STEEM blockchain.

---

## Contributing
If you find any issues or have suggestions for improvement, feel free to open an issue or submit a pull request.
https://steemit.com/@dhaka.witness
