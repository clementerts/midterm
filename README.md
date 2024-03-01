# midterm
#question 1
a = 6

a = a - 2

print(a*2)

a = a * 2

print(a+1)

a = a // 3

#question 2
print((2+3)*6/2 and 18.0) 

#question 3
import datetime
a = 7
b = 2
today = datetime.datetime.today()
day_of_week = today.weekday()
month_of_year = today.month
a = a + day_of_week
b += month_of_year
 
print(a)
print(b)
c = a + b
print(c)
d = "xyz" * (c//3)
print(d)


def palindrome(word):
    if word == word[::-1]:
        return True
    else:
        return False

palindrome(8025833559061079503003059701609553385208)

80258335590610795030
03059701609553385208          yes

54858398375010700450          yes
05400701057389385845

65930366013593433746          yes
64733439531066303956

74896177197492446463
36564429479177169847


#question 8
s = "http://google.com and then there could be http://yahoo.com or even a website like http://bbc.co.uk"
start = 0
while True:
    start = s.find("http://", start)
    if start == -1:
        break
    end = s.find(" ",start)
    if end == -1:
        print(s[start:])
        break
    print(s[start:end])
    start = end

#question 9
from datetime import datetime

def days_passed_since_birthday(birthday):
    birthday_date = datetime.strptime(birthday, "%d-%m-%Y")
    current_date = datetime.now()
    birthday_this_year = datetime(current_date.year, birthday_date.month, birthday_date.day)
    if current_date < birthday_this_year:
        birthday_this_year = datetime(current_date.year - 1, birthday_date.month, birthday_date.day)
    days_passed = (current_date - birthday_this_year).days
    total_days_passed = days_passed - (current_date.year - birthday_date.year) * 365
    return total_days_passed

birthday = "04-07-2000"
print("Days passed since your birthday:", days_passed_since_birthday(birthday))
