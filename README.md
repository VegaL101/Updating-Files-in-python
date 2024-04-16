# Updating-Files-in-python


## Objective

Certain content is restricted and is only accessed by IPs on a allowed list. The file “allow_list.txt” holds all the IPs. There is also a remove list containing IPs that should no longer have access to restricted content. The algorithm in this project automatically removes IPs in that list that should no longer have access to the content.

### Skills Learned

- Learned how to access and rewrite files in python.
- Gain an understanding on how to automate tasks.

## Steps

Step 1:
Opening and reading the file contents

Firstly I assigned the “allow_list.txt” file to the import_file variable. After that I proceeded to open the file with the code below.
 
 ![python pt 1](https://github.com/VegaL101/Updating-Files-in-python/assets/166334918/e23f3a6c-f2f4-4f7b-a676-4d41b5450cdb)

The with statement is used with the .open()  function to open and read the contents of the file. The output of the code is stored within a file variable which has the .read()  function applied to it which converts the file to a string which can be read. Then we assign that within the ip_addresses variable.

Step 2:
Convert the string into a list

Next in the algorithm we transform the string into a list using the .split() function and apply it to ip_addresses .

![python 2](https://github.com/VegaL101/Updating-Files-in-python/assets/166334918/1d09da46-eb51-4067-801d-3bd47e81cbca)

The purpose of this is to make it easier to remove ip addresses that are no longer allowed on the file. By default, the .split() function separates the text by whitespace and turns them into individual elements. In this case we make each ip address its own element and then proceed to store it within ip_addresses again.

Step 3:
Going through the list and removing IP addresses

![python 3](https://github.com/VegaL101/Updating-Files-in-python/assets/166334918/ef708dc7-b1bf-45dc-a355-0ee0aa78e574)

After converting the file from a string to a list we can begin the next part of the algorithm.
I will be using a for loop to go through the ip addresses and find any ip addresses that are on the remove list.

In the loop the key words for, and in are used with elements, and ip_addresses. Elements being the variable for each IP address in  ip_addresses which is the file it's going through. The algorithm then removes any ip addresses using the if conditional statement. If any of the elements from ip_addresses are found in remove_list they will be taken out of the file using the .remove() function. Which is applied to ip_addresses.

STEP 4:
Updating the file

![python 4](https://github.com/VegaL101/Updating-Files-in-python/assets/166334918/0e1e781e-eeda-47f1-a66f-82c81d0a6642)

To finalize and update the file containing the revised lists of IP addresses we wanna use the .join() function. What this function does is convert all the items we have back into a string. Which is applied to our variable as shown below. We use the string “\n” to let python know to place each element in a new line.

Using the “w” argument with the open() function indicates that I want to open the file and rewrite its contents. Using the the .with() function with our ip_addresses variable as the argument we can apply this to our file object as shown above.This tells python that ip_addresses and its contents will replace the data in the file used with our with statement.

Summary:
I Created this algorithm so that we may remove any ip addresses found in the  remove_list variable from the  “allow_list.txt” file . This algorithm involves opening the file, converting to a string so that it may be read, and then converting it once more into a list stored in the ip_addresses variable. I then used a for loop with a conditional statement that will check and find any ip addresses in the remove_list that are inside the ip_addresses variable. I then applied the .remove()  function to remove any elements from the  remove_list found in ip_addresses. After this was done the final steps were to use the .join() function convert ip_addresses into a string.Finishing this, i used the .write() function to rewrite and update the contents of the  “allow_list.txt” file to the new and revised list.8



