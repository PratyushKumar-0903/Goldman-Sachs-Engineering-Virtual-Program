# Goldman-Sachs-Virtual-Intern

## Goldman-Sachs-Crack-Leaked-Passsword-Database
## Password Controls and Security Policies

### Overview 
As a governance analyst it is part of your duties to assess the level of protection offered by implemented controls and minimize the probability of a successful breach. You often need to know the techniques used by hackers to circumvent implemented controls and propose uplifts to increase the overall level of security in an organization. Gaining valid credentials gives the attackers access to the organization’s IT system, thus circumventing most of perimeter controls in place.

## Project Objectuve
`What type of hashing algorithm was used to protect passwords?`

`What level of protection does the mechanism offer for passwords?`

`What controls could be implemented to make cracking much harder for the hacker in the event of a password database leaking again?`

`What can you tell about the organization’s password policy (e.g. password length, key space, etc.)?`

`What would you change in the password policy to make breaking the passwords harder? `

Here is a sample data file containing hashes dumped together:

https://github.com/PratyushKumar-0903/Goldman-Sachs-Engineering-Virtual-Program/blob/master/Password_Dump.txt

After the conducted analysis it was determined that organization uses an outdated password hashing algorithm (MD5) which offers very little protection in the event of a password database leaking. It was also determined that the current password policy is not aligned with industry best practices allowing users to have short passwords (6 characters) and reuse usernames as part of passwords. 

As a result of the analysis the following uplifts are proposed to increase the overall level of password protection: 

•	Use a dedicated password hashing algorithm bcrypt, scrypt or PBKDF2 as this will greatly increase the time needed to crack individual passwords,

•	Implement salting to prevent usage of rainbow tables to speed up cracking,

•	Increase the minimum password length requirement to 10 characters – this will increase the computational effort required to crack password and will give additional time to change all passwords in the event of the password database being leaked,

•	Prevent passwords to be the same as usernames or reused as part of the password – such password combination is easy to check without gaining access to the password database itself.  

•	It is advised to educate users on creating safe and easy to remember passwords. Having a password policy requiring long passwords with a number of special characters results in user writing passwords down or constantly resetting them. The best way to create a strong and user-friendly password is using passphrases (e.g.  mygrannyschairhadstaples). The best way to create such passwords is to combine a couple of completely random word. It’s also advised to use some special characters and numbers as easy to remember substitutions to expand the key space (e.g. mYgranny$cha1rhadstaples)

•	Educate users on the benefits of passwords managers. Having a password manager allows having very long and completely random passwords (e.g. M>?{tk6Cfep6BrZ4J)KZWQ8j) without the need to remember/write down. A strong passphrase is still required as a master key for to access the password manager.

# Project Report and Observations 
Completing this task assigned by Goldman Sachs, MD5 and SHA were the two algorithms that I came across. Analysing the passwords and their respective security algorithms used, I narrowed down my observations into this report.

## Project Report
```
Subject: Crack leaked password database

Dear Sir/Ma’am,
While cracking and reviewing the leaked hashes, I have found multiple loopholes and vulnerabilities in the shared password list. 
Please find the below suggestions and ideas to further improve the password selection process and make breaking the passwords 
more difficult.

All the compromised passwords are using the MD5 cryptographic hash function which has many weaknesses, the main issue being MD5 
is vulnerable to collision attacks in which the hashing algorithm takes two different inputs and produces the same hash. This 
property means the MD5 hash function is considered “broken” and very high-risk. This provides very poor level of protection as 
multiple tools such as Hashcat and free-to-use web apps can be used to crack the hashes.
I used Hashcat along with CrackStation’s Human only dictionary and MD5 Online to crack these.

To make breaking the passwords harder, a lower-risk hash function should be implemented such as SHA512crypt which is resistant 
to collision attacks and mostly resistant to length extension attacks, or Bcrypt which is the standard password hash algorithm 
used in most systems. SHA512crypt passes the password through 5,000 hashing iterations to make decrypting harder and near 
impossible. Bcrypt includes a salt and is designed to withstand brute-force attacks by intentionally being slower to operate. 
The unsalted passwords listed below could be cracked using online websites such as CrackStation, which is very insecure. 

Judging from the cracked passwords listed below, the password policy allows employees to use any combination of numbers and 
characters. The space character is not a valid input, and the minimum password length may be six and the maximum fourteen, 
although the size of the sample passwords is too small for this conclusion to be definitive. The organisation’s average password 
length is almost eight characters but has multiple passwords shorter than eight and easy to guess which pose a high security 
risk. Their key space is smaller than modern standards.

The password policy should be changed so that passwords include the following: 
• Use of number, letter, special character, capital letter
• Keeping a threshold on length. Set minimum length of 8. 
• Employees should also avoid easy to guess passwords such as pet names and birthdates as well as avoid repeating their 
  passwords for multiple accounts.
• Reduce redundancy across services such that in case of a leak out of one service doesn’t make the other passwords 
  vulnerable.
• Not allowing sibling credentials to assist the password naming, like name / user name / email / date of birth / sex.
• Avoiding the occurrence of English verbs like book, popular, eating, hero, life, John Wick, crack me, expert that makes 
  the password vulnerable to brute force attacks.

Fond regards,
Pratyush Kumar

```
## Observations:
```
Security Algorithms used: 
experthead:e10adc3949ba59abbe56e057f20f883e – MD5
interestec:25f9e794323b453885f5181f1b624d0b – MD5
ortspoon:d8578edf8458ce06fbc5bb76a58c5ca4 –MD5
reallychel:5f4dcc3b5aa765d61d8327deb882cf99 –MD5
simmson56:96e79218965eb72c92a549dd5a330112 – MD5
bookma:25d55ad283aa400af464c76d713c07ad – MD5 
popularkiya7:e99a18c428cb38d5f260853678922e03 – MD5
eatingcake1994:fcea920f7412b5da7be0cf42b8c93759 – MD5 
heroanhart:7c6a180b36896a0a8c02787eeafb0e4c – MD5
edi_tesla89:6c569aabbf7775ef8fc570e228c16b98 – MD5
liveltekah:3f230640b78d7e71ac5514e57935eb69 – MD5
blikimore:917eb5e9d6d6bca820922a0c6f7cc28b – MD5
johnwick007:f6a0cb102c62879d397b12b62c092c06 – MD5
flamesbria2001:9b3b269ad0a208090309f091b3aba9db – MD5
oranolio:16ced47d3fc931483e24933665cded6d - MD5
spuffyffet:1f5c5683982d7c3814d4d9e6d749b21e - MD5
moodie:8d763385e0476ae208f21bc63956f748 - MD5
nabox:defebde7b6ab6f24d5824682a16c3ae4 - MD5
bandalls:bdda5f03128bcbdfa78d8934529048cf - MD5

Cracked Passwords:
experthead:e10adc3949ba59abbe56e057f20f883e - 123456
interestec:25f9e794323b453885f5181f1b624d0b - 123456789
ortspoon:d8578edf8458ce06fbc5bb76a58c5ca4 - qwerty
reallychel:5f4dcc3b5aa765d61d8327deb882cf99 - password
simmson56:96e79218965eb72c92a549dd5a330112 - 111111
bookma:25d55ad283aa400af464c76d713c07ad - 12345678
popularkiya7:e99a18c428cb38d5f260853678922e03 - abc123
eatingcake1994:fcea920f7412b5da7be0cf42b8c93759 - 1234567
heroanhart:7c6a180b36896a0a8c02787eeafb0e4c - password1
edi_tesla89:6c569aabbf7775ef8fc570e228c16b98 - password!
liveltekah:3f230640b78d7e71ac5514e57935eb69 - qazxsw
blikimore:917eb5e9d6d6bca820922a0c6f7cc28b - Pa$$word1
johnwick007:f6a0cb102c62879d397b12b62c092c06 - bluered
```
Complete report and my findings are available at: 

https://github.com/PratyushKumar-0903/Goldman-Sachs-Engineering-Virtual-Program


## Completion Certificate

https://forage-uploads-prod.s3.amazonaws.com/completion-certificates/Goldman%20Sachs/NPdeQ43o8P9HJmJzg_Goldman%20Sachs_FYquW8LGzsM8QppmQ_1651005195990_completion_certificate.pdf


## Resources 

https://arstechnica.com/information-technology/2013/05/how-crackers-make-minced-meat-out-of-your-passwords/

https://www.security.org/how-secure-is-my-password/

https://en.wikipedia.org/wiki/Cryptographic_hash_function

https://en.wikipedia.org/wiki/Salt_(cryptography)

https://en.wikipedia.org/wiki/Password_cracking#Software
