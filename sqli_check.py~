#Soumyargha Sinha
import re
import urllib.request

url = input("Enter the url to check for SQLI vulnerability : ")
a = "'"
final = url + a
b = 0
errors = {'error in your SQL syntax','mysql_fetch_array()','mysql_fetch_assoc()','An error occurred','session_start()','mysql_query()','mysql_num_rows','mysql_fetch_row','Unknown Column','SQL Error','mysql_free_result'}
header = {'User-Agent': 'Mozilla/5.0'}
for i in errors:
        query = urllib.request.Request(final,headers=header)
        msg = urllib.request.urlopen(query)
        msgread = msg.read()
        if re.search(str(i), str(msgread)):
            print("\nThe site is vulnerable.\n")
            print("The error found is : "+i+"\n")
            b = 1
            break

if (b == 0):
    print("Could not find any vulnerability, checking from the error list. \n")
            
            
