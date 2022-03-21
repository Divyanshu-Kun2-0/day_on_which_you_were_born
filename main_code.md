tarikh=int(input("Enter the date(dd) on which you were born : "))
mahina=int(input("Enter the month(mm) on which you were born (numeric value) "))
year=int(input("Enter the year you were born "))
leap_year=0
days_old=0
for i in range(year,2022):
	if i%4==0 and i%400!=0:
		leap_year+=1
if year%4==0 :
	if year%100==0 and year%400==0:
		if mahina >=3 or (mahina==2 and tarikh==29):
			pass
		else:
			days_old+=1

days_old+=((366*(leap_year))+365*(2022-year-leap_year))
if mahina==1:
	days_old-=tarikh
elif mahina==2:
	days_old-=(31+tarikh)
elif mahina==3:
	days_old-=(59+tarikh)
elif mahina==4:
	days_old-=(90+tarikh)
elif mahina==5:
	days_old-=(120+tarikh)
elif mahina==6:
	days_old-=(151+tarikh)
elif mahina==7:
	days_old-=(181+tarikh)
elif mahina==8:
	days_old-=(212+tarikh)
elif mahina==9:
	days_old-=(243+tarikh)
elif mahina==10:
	days_old-=(273+tarikh)
elif mahina==11:
	days_old-=(304+tarikh)
else :
	days_old-=(334+tarikh)
if mahina>=3 and year%4==0 and year%400!=0:
	days_old-=1
days_old+=1
decider=days_old%7
posibility=["saturday","friday","thursday","wednesday","tuesday","monday","sunday"]
print("you have lived",days_old,"days(with respect to 1 january 2022)")
print("and you were born on",posibility[decider])
