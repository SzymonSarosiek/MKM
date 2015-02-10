# mkm_api
MagicCardMarket API 1.1 accesser

This program is a simple executable file to communicate simply with the MKM API v1.1. 
You provide the program with accesss tokens (https://www.magiccardmarket.eu/?mainPage=showMyAccount)
and then issues commands to access resources in the API (https://www.mkmapi.eu/ws/documentation/API_1.1:Main_Page)


Usage: 

       MKM <CMD> <RESOURCE> [-f FILE] [DATA]

Availible CMD: GET, PUT, POST, DEL

For resources check https://www.mkmapi.eu/ws/documentation/API_1.1:Main_Page

PUT and POST requires data, from either a file (-f) or given text (DATA).

All data should be given/received as UTF8

If tokens.txt does not exist, the program will pause while it waits for you to
fill in the created tokens.txt file:
      
      URL=https://www.mkmapi.eu/ws/v1.1/
      App token=YOUR APP TOKEN
      App secret=YOUR APP SECRET
      Access token=YOUR ACCESS TOKEN
      Access token secret=YOUR ACCESS TOKEN SECRET

Examples:
      
        MKM GET account
      
        MKM GET stock/1
      
        MKM DEL shoppingcart
      
        MKM GET orders/2/8 > received.txt
        
4 .bat files are included, with simple functionality:

  * empty_cart.bat - empties your shopping cart
  * get_orders.bat - retrieves all your orders
  * get_stock.bat - retrives all your stocks to stock.xml. Stock.xml can be opened and edited using f.ex. Microsoft Excel
  * update_stock.bat - uploads stock.xml. This updates all existing stocks
