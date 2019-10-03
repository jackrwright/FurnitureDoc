# Furniture Pricer Suite
I wrote these apps to aid in the processing and sale of furniture donations.

## The Apps
### Pricer
The Pricer app is designed to run on an iPhone/iPod and allows employees to create a record for each furniture item to be sold. A unique item number is automatically created by the MySQL server.
The fields to be filled in by the employee are:

* Description
* Price
* Photo

The photo is captured using the standard UIImagePickerController API. Photos are stored in a separate folder on the server rather than in the MySQL database:

![Image of Pricer screen](https://github.com/jackrwright/FurniturePricer/blob/master/PricerScreen.jpg)

Once the fields are complete, a card is printed to be attached to the furniture item:

![Image of furniture card](https://github.com/jackrwright/FurniturePricer/blob/master/furnitureCard.jpg)

The card is taken by the customer to the register for purchase.

In addition to creating furniture item records, the user can view existing items with filters available for:

* Today
* This Week
* All
* Delivered

![Image of furniture item list](https://github.com/jackrwright/FurniturePricer/blob/master/itemList.jpg)

Tapping on an item in the list displays its details and allows the user to print the item or mark it 'delivered'.

![Image of item detail](https://github.com/jackrwright/FurniturePricer/blob/master/itemDetail.jpg)

Tapping on Edit here presents an Edit view controller to allow editing of the description, price or replacing the photo. The item may also be deleted here.

![Image of item edit](https://github.com/jackrwright/FurniturePricer/blob/master/editItem.jpg)


### Will Call
The Will Call app is designed to run on an iPad and allows will call staff to record the delivery of an item to the customer.
The customer presents to the employee the furniture card printed earlier by the Pricer app. It contains a QR barcode containing the item number. Once scanned, the item is retrieved from the database and it's info and photo are presented in the app. The employee locates the item based on the photo and delivers it to the customer. The employee then taps the delivered button to record the delivery date and time.

![Image of Will Call](https://github.com/jackrwright/FurniturePricer/blob/master/willCall.jpg)
