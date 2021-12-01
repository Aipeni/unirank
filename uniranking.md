```python
import requests
from bs4 import BeautifulSoup
import pandas_datareader as pdr
import pandas as pd
```


```python

import requests
from bs4 import BeautifulSoup
url='https://studyabroad.shiksha.com/usa/universities/harvard-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
uni=[]
harvard=rank[rank.index("MBA"):rank.index("Bachelors in Near Eastern Languages and Civilizations")+1]
i=0
while i < len(harvard):
    uni.append("Harvard University")
    i +=1
df=pd.DataFrame({"program":harvard,"University":uni})
```


```python
url='https://studyabroad.shiksha.com/usa/universities/arizona-state-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
asu=rank[rank.index("MS Computer Science"):rank.index("Creative Writing, MFA")+1]
uni=[]
i=0
while i < len(asu):
    uni.append("Arizona State University")
    i +=1
df2=pd.DataFrame({"program":asu,"University":uni})
list1 = pd.concat([df,df2])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/stanford-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
su=rank[rank.index("Master of Science in Computer Science"):rank.index("Master of Arts in Art Practice")+1]
uni=[]
i=0
while i < len(su):
    uni.append("Stanford University")
    i +=1
df3=pd.DataFrame({"program":su,"University":uni})
list1 = pd.concat([list1,df3])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/texas-a-m-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
tam=rank[rank.index("Master of Science in Computer Science"):rank.index("BS in Public Health and Master of Public Health in Epidemiology")+1]
uni=[]
i=0
while i < len(tam):
    uni.append("Texas A&M University")
    i +=1
df4=pd.DataFrame({"program":tam,"University":uni})
list1 = pd.concat([list1,df4])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/massachusetts-institute-of-technology/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
mit=rank[rank.index("Bachelors of Computer Science and Engineering "):rank.index("Bachelor of Science in Asian and Asian Diaspora Studies")+1]
uni=[]
i=0
while i < len(mit):
    uni.append("Massachusetts Institute of Technology (MIT)")
    i +=1
df5=pd.DataFrame({"program":mit,"University":uni})
list1 = pd.concat([list1,df5])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/the-university-of-texas-at-austin/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
texas=rank[rank.index("Master of Science in Computer Science"):rank.index("Master of Fine Arts in Playwriting")+1]
uni=[]
i=0
while i < len(texas):
    uni.append("University of Texas at Austin")
    i +=1
df6=pd.DataFrame({"program":texas,"University":uni})
list1 = pd.concat([list1,df6])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/university-of-illinois-chicago-campus/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
chi=rank[rank.index("MS in Computer Science"):rank.index("Joint BA in Urban Studies/Master of Urban Planning and Policy")+1]
uni=[]
i=0
while i < len(chi):
    uni.append("University of Illinois, Chicago (UIC)")
    i +=1
df8=pd.DataFrame({"program":chi,"University":uni})
list1 = pd.concat([list1,df8])
```


```python
#url='https://studyabroad.shiksha.com/usa/universities/california-state-university-los-angeles-campus/courses'
#headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
#r = requests.get(url, headers=headers)
#sp=BeautifulSoup(r.text, 'lxml')
#datas=sp.find_all('a', sa="int")
#rank=[]
#for i in range(0,len(datas)):
    #try:
        #rank.append(datas[i].text)
    #except:
        #break
#CSULA=rank[rank.index("MS in Computer Science"):rank.index("Bachelor of Science Degree in Kinesiology")+1]
#uni=[]
#i=0
#while i < len(CSULA):
    #uni.append("California State University Los Angeles Campus")
    #i +=1
#df10=pd.DataFrame({"program":CSULA,"University":uni})
#list1 = pd.concat([list1,df10])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/new-york-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
NYU=rank[rank.index("MBA"):rank.index("BSc in Sustainable Urban Environments/MS in Applied Urban Science")+1]
uni=[]
i=0
while i < len(NYU):
    uni.append("New York University (NYU)")
    i +=1
df11=pd.DataFrame({"program":NYU,"University":uni})
list1 = pd.concat([list1,df11])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/university-of-southern-california/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
USC=rank[rank.index("Master of Science in Computer Science "):rank.index("Bachelor of Science in Electrical Engineering")+1]
uni=[]
i=0
while i < len(USC):
    uni.append("University of Southern California")
    i +=1
df12=pd.DataFrame({"program":USC,"University":uni})
list1 = pd.concat([list1,df12])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/georgia-institute-of-technology/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
git=rank[rank.index("Master of Science in Computer Science"):rank.index("Masters of City and Regional Planning + MS Public Policy")+1]
uni=[]
i=0
while i < len(git):
    uni.append("Georgia Institute of Technology (Georgia Tech)")
    i +=1
df14=pd.DataFrame({"program":git,"University":uni})
list1 = pd.concat([list1,df14])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/university-of-california-berkeley-campus/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Science in Computer Science"):rank.index("Bachelor of Arts (BA) in Applied Mathematics")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of California, Berkeley (UCB)")
    i +=1
df20=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df20])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/purdue-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Science in Computer Science"):rank.index("Bachelor of Arts in Digital Criminology")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Purdue University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/columbia-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MS in Computer Science"):rank.index("MA in Bilingual/Bicultural Childhood Special Education (BiSPED)")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Columbia University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/university-of-california-los-angeles-campus/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Science in Computer Science"):rank.index("Education and Social Transformation BA")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of California, Los Angeles (UCLA)")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/boston-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MS in Computer Science"):rank.index("BS in Communication")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Boston University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/university-of-florida/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("M.S. in Computer Science"):rank.index("BS in Horticultural Science")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Florida")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/university-of-michigan/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MS Computer Science and Engineering"):rank.index("Master of Science in Athletic Training")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Michigan")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/north-carolina-state-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Computer Science-Track in Software Engineering"):rank.index("Master of Science in Comparative Biomedical Sciences")+1]
uni=[]
i=0
while i < len(a):
    uni.append("North Carolina State University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/university-of-illinois-urbana-campus/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Science in Computer Science"):rank.index("Bachelor of Science in Liberal Arts and Sciences in Statistics and Computer Science")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Illinois at Urbana-Champaign")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/university-of-pennsylvania/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Business Administration"):rank.index("Near Eastern Languages and Civilizations, MA")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Pennsylvania")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/university-of-washington/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MS in Computer Science & Engineering"):rank.index("MS in Pediatric Dentistry")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Washington")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/university-of-maryland/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("M.S in Computer Science"):rank.index("B.S. in Electrical Engineering")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Maryland, College Park")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/carnegie-mellon-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("M.S. in Computer Science"):rank.index("Primary Master of Science in Machine Learning")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Carnegie Mellon University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/university-of-california-san-diego-campus/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Science in Computer Science"):rank.index("MS Geophysics")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of California, San Diego (UCSD)")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/yale-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MBA"):rank.index("Graduate Entry Prespecialty in Nursing (GEPN)/Master of Public Health (MPH)")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Yale University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/michigan-state-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Science in Computer Science"):rank.index("BA in Child Development")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Michigan State University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/university-of-arizona/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MS Computer Science"):rank.index("Certificate in Heritage Conservation")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Arizona")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/the-university-of-chicago/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Full-Time MBA"):rank.index("BA/MA in the Social Sciences")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Chicago")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/university-of-massachusetts-amherst/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MS in Computer Science"):rank.index("MBA with MS in Environmental Engineering")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Massachusetts, Amherst")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/university-of-wisconsin-madison/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Computer Sciences M.S"):rank.index("Classics, BA/BS")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Wisconsin-Madison")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/princeton-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Science in Engineering Computer Science"):rank.index("Bachelor of Arts in Public and International Affairs")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Princeton University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/ohio-state-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master in Computer Science and Engineering"):rank.index("MA in Woodwind Pedagogy")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Ohio State University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/pennsylvania-state-university-university-park/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Science in Computer Science and Engineering"):rank.index("BS in World Language (K-12) Education")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Pennsylvania State University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/northwestern-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Science in Computer Science"):rank.index("Bachelor of Science in Learning Sciences")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Northwestern University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/california-institute-of-technology/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Bachelor of Science in Computer Science"):rank.index("Bachelor of Science in Applied and Computational Mathematics")+1]
uni=[]
i=0
while i < len(a):
    uni.append("California Institute of Technology (Caltech)")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/usa/universities/duke-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("M.S in Computer Science "):rank.index("B.S.E + M.S in Civil Engineering")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Duke University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/university-of-bristol/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MSc Management"):rank.index("MSc Image and Video Communications and Signal Processing")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Bristol")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/university-of-glasgow/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MBA"):rank.index("Public Policy & Management MSc/PGDip")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Glasgow")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/university-of-leeds/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Full Time MBA"):rank.index("Chemical and Materials Engineering MEng")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Leeds")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/university-of-warwick/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Business Administration"):rank.index("Mathematics (Diploma plus MSc)")+1]
uni=[]
i=0
while i < len(a):
    uni.append("The University of Warwick")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/university-of-nottingham/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Bsc Nursing (Adult)"):rank.index("Master of Public Administration PGDip")+1]
uni=[]
i=0
while i < len(a):
    uni.append("The University of Nottingham")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/university-of-york/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MSc in Management"):rank.index("BSc (Hons) Economics and Mathematics")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of York")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/university-of-southampton/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MSc Business Analytics and Management Sciences"):rank.index("BSc (Hons) Psychology")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Southampton")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/lancaster-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Full-time MBA"):rank.index("Nuclear Engineering BEng Hons")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Lancaster University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/the-university-of-sheffield/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MBA"):rank.index("Bachelors of Environmental Science")+1]
uni=[]
i=0
while i < len(a):
    uni.append("The University of Sheffield")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/university-of-leicester/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MSc Advanced Computer Science"):rank.index("MEng in Mechanical Engineering")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Leicester")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/university-of-exeter/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Full-time MBA"):rank.index("MRes inGlobal Political Economy")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Exeter")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/durham-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MBA Full-Time "):rank.index("Msci Chemistry and Maths")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Durham University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/university-of-bath/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Full-time MBA"):rank.index("MPharm (Hons)")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Bath")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/the-university-of-liverpool/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master in Management (MIM)"):rank.index("BA (Hons) in Philosophy with Game Design Studies")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Liverpool")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/king-s-college-london/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Medicine MBBS"):rank.index("China & Globalisation MSc")+1]
uni=[]
i=0
while i < len(a):
    uni.append("King's College London (KCL)")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/the-university-of-edinburgh/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Business Administration"):rank.index("LLM Corporate Law")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Edinburgh")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/imperial-college/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Full-Time MBA"):rank.index("MEng Mathematics and Computer Science")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Imperial College London")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/university-college-london/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Business Administration MBA"):rank.index("Computational Statistics and Machine Learning MSc")+1]
uni=[]
i=0
while i < len(a):
    uni.append("UCL (University College London)")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/university-of-cambridge/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Business Administration"):rank.index("AdvDip in Hebrew Studies")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Cambridge")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/university-of-oxford/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MBA"):rank.index("MSc in Archaeological Science")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Oxford")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/university-of-manchester/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MBA"):rank.index("MRes Experimental Medicine (Musculoskeletal)")+1]
uni=[]
i=0
while i < len(a):
    uni.append("The University of Manchester")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/london-school-of-economics-and-political-science/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MSc in Management"):rank.index("MPhil Environmental Policy and Development")+1]
uni=[]
i=0
while i < len(a):
    uni.append("London School of Economics and Political Science (LSE)")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/newcastle-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Business Administration"):rank.index("International Legal Studies LLM")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Newcastle University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/queen-mary-university-of-london/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MSc Management "):rank.index("BEng (Hons) Materials Science and Engineering")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Queen Mary University of London (QMUL)")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/university-of-birmingham/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MBA International Business"):rank.index("MA Literature and Culture")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Birmingham")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/university-of-st-andrews/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MLitt in Management"):rank.index("Master of Arts (Honours) Film Studies and Modern History")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of St Andrews")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/university-of-surrey/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Business Analytics MSc "):rank.index("Bachelors of Automotive Engineering BEng (Hons) ")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Surrey")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/university-of-sussex/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MSc in Management"):rank.index("BSc(Hons) in Games and Multimedia Environments")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Sussex")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/loughborough-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Business Administration"):rank.index("MA in Security")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Loughborough University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/cardiff-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MBA"):rank.index("PgDip in Social Science Research Methods (Environmental Planning)")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Cardiff University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/queen-s-university-belfast/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Business Administration"):rank.index("MPlan in European Planning")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Queen's University of Belfast")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/university-of-aberdeen/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Masters of Business Administration"):rank.index("MA in Film & Visual Culture and Philosophy")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Aberdeen")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/uk/universities/university-of-reading/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MSc in Food Science"):rank.index("Post Graduate Certificate in Education in Secondary Science: Physics")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Reading")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/canada/universities/university-of-toronto/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MSc Computer Science"):rank.index("BSc Hons in Bioinformatics and Computational Biology")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Toronto")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/canada/universities/mcgill-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Science in Computer Science"):rank.index("Master of Arts (M.A.) Second Language Education")+1]
uni=[]
i=0
while i < len(a):
    uni.append("McGill University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/canada/universities/university-of-british-columbia/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Science in Computer Science"):rank.index("Bachelor of Arts in Language")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of British Columbia")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/canada/universities/university-of-alberta/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MBA"):rank.index("BA in Environmental Studies")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Alberta")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/canada/universities/university-of-montreal/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Science in Economics"):rank.index("BA in Sociology")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Université de Montréal")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/canada/universities/mcmaster-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MSc in Computer Science"):rank.index("Combined Honours in Peace Studies and Another Subject (B.A.)")+1]
uni=[]
i=0
while i < len(a):
    uni.append("McMaster University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/canada/universities/university-of-waterloo/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Data Science and Artificial Intelligence - MDSAI"):rank.index("Bachelors of Arts in Peace and Conflict Studies")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Waterloo")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/canada/universities/western-university-canada/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Science in Computer Science"):rank.index("Master of Arts in Linguistics")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Western University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/canada/universities/university-of-calgary/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Science in Computer Science"):rank.index("Bachelor of Science in Chemistry")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Calgary")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/canada/universities/queen-s-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("MSc in Computing"):rank.index("BA in Music Theatre")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Queen's University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/canada/universities/dalhousie-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Applied Computer Science "):rank.index("BA in History of Science and Technology")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Dalhousie University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/australia/universities/the-university-of-melbourne/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Full-Time MBA"):rank.index("Graduate Diploma in Surgical Anatomy")+1]
uni=[]
i=0
while i < len(a):
    uni.append("The University of Melbourne")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/australia/universities/the-university-of-sydney/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Data Science"):rank.index("Master of Emergency Nursing")+1]
uni=[]
i=0
while i < len(a):
    uni.append("The University of Sydney")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/australia/universities/rmit-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Business Administration"):rank.index("Diploma of Conservation and Land Management")+1]
uni=[]
i=0
while i < len(a):
    uni.append("RMIT University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/australia/universities/the-university-of-queensland/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Business Administration"):rank.index("Graduate Certificate in Food Science and Technology")+1]
uni=[]
i=0
while i < len(a):
    uni.append("The University of Queensland (UQ)")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/australia/universities/monash-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Business Administration"):rank.index("Bachelor of Education (Honours) and Bachelor of Science")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Monash University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/australia/universities/the-university-of-adelaide/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Bachelor of Nursing"):rank.index("Bachelor of Science in Geophysics")+1]
uni=[]
i=0
while i < len(a):
    uni.append("The University of Adelaide")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/australia/universities/curtin-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Business Administration"):rank.index("Bachelor of Laws, Bachelor of Arts")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Curtin University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/australia/universities/macquarie-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Business Administration"):rank.index("Bachelor of Arts in Creative Writing")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Macquarie University")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/australia/universities/queensland-university-of-technology/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Bachelor of Nursing"):rank.index("Bachelor of Engineering (Honours)/Bachelor of Science")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Queensland University of Technology (QUT)")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/australia/universities/university-of-wollongong/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Bachelor of Nursing"):rank.index("Master of Engineering (Mechatronic Engineering)")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Wollongong")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/australia/universities/the-university-of-newcastle/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Business Administration (Global)"):rank.index("Bachelor of Communication")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Newcastle")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/australia/universities/university-of-technology-sydney/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Business Administration"):rank.index("Bachelor of Management Bachelor of Arts in International Studies")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Technology Sydney (UTS)")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/australia/universities/the-university-of-western-australia/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Business Analytics"):rank.index("Bachelor of Philosophy (Hons) in Anatomy and Human Biology")+1]
uni=[]
i=0
while i < len(a):
    uni.append("The University of Western Australia (UWA)")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/australia/universities/university-of-new-south-wales/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("AGSM MBA (full-time)"):rank.index("Master of Engineering Science")+1]
uni=[]
i=0
while i < len(a):
    uni.append("The University of New South Wales (UNSW)")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/australia/universities/australian-national-university/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Business Administration"):rank.index("Master of Diplomacy")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Australian National University (ANU)")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/new-zealand/universities/university-of-auckland/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Science in Computer Science"):rank.index("Bachelor of Science in Physics")+1]
uni=[]
i=0
while i < len(a):
    uni.append("The University of Auckland")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/new-zealand/universities/university-of-otago/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Full-Time MBA"):rank.index("Bachelor of Science (BSc) majoring in Mathematics")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Otago")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/new-zealand/universities/victoria-university-of-wellington/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Executive MBA"):rank.index("Master of Laws – LLM")+1]
uni=[]
i=0
while i < len(a):
    uni.append("Victoria University of Wellington")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/new-zealand/universities/university-of-canterbury/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Business Administration"):rank.index("Master of Forestry Science")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Canterbury")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python
url='https://studyabroad.shiksha.com/new-zealand/universities/university-of-waikato/courses'
headers = {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/50.0.2661.102 Safari/537.36'}
r = requests.get(url, headers=headers)
sp=BeautifulSoup(r.text, 'lxml')
datas=sp.find_all('a', sa="int")
rank=[]
for i in range(0,len(datas)):
    try:
        rank.append(datas[i].text)
    except:
        break
a=rank[rank.index("Master of Business Administration (MBA)"):rank.index("LLM Master of Laws")+1]
uni=[]
i=0
while i < len(a):
    uni.append("University of Waikato")
    i +=1
df=pd.DataFrame({"program":a,"University":uni})
list1 = pd.concat([list1,df])
```


```python

```


```python

```


```python
len(a)
```




    29




```python
master=[]
bacholer=[]
gc=[]
asso=[]
llm=[]
```


```python
for i in list1["program"]:
    if "Master" in i or "MBA" in i or "MS" in i or "MPS" in i or"MFA" in i or"MD" in i or"MA" in i or "MEng" in i or "M.S." in i or "M.S" in i or "MEd" in i or "M.B.A." in i or "MPH" in i or "M.Ed." in i or "M.A." in i or "M.P.H." in i or "M.F.A." in i or "M.H.A." in i or "M.U." in i or "M.P.A.S." in i or "M.M." in i or "M.Eng." in i or "M.E.T" in i or "MPA" in i or "M.P.A." in i or "MHS" in i or "MHS" in i or "M.Eng" in i or "MENg" in i or "M.A" in i or "M.I.S." in i or "M.F.A" in i or "M.I.S." in i or "M.Ed" in i or "M.E." in i or "M.ENG" in i or "M.P.P.A" in i or "M.P.W" in i or "MBE" in i or "MCIT" in i or "MBIOT" in i or "MBDS" in i or "MIPD" in i or "MBE" in i or "MRA" in i or "MPhil" in i or "MUSA" in i or "MLA" in i or "ML" in i or "MCP" in i or "MBMI" in i or "MHQS" in i or "MPhilEd" in i or "MTESOL" in i or "M. S." in i or "MM" in i or "Maaster" in i or "M. Tech" in i or "Med" in i or "N.D.S." in i or "M.D." in i or "M.P.S" in i: 
        master.append("master")
        bacholer.append("")
        gc.append("")
        asso.append("")
        llm.append("")
    elif "Bachelor" in i or "BS" in i or "BA" in i or "BFA" in i or "BLA" in i or "B.S." in i or "B.S" in i or "Bacherlors" in i or "B.A" in i or "B.B.A." in i or "B.A." in i or "B.F.A." in i or "B.I.S." in i or "B.M." in i or "BNS" in i or "BE" in i or "B.Des" in i or "BHS" in i or "B.F.A" in i or "BEng" in i or "BM" in i or "BDes" in i:
        bacholer.append("bacholer")
        master.append("")
        gc.append("")
        asso.append("")
        llm.append("")
    elif "Graduate Certificate" in i or "Certificate" in i or "Certification" in i:
        gc.append("Graduate Certificate")
        master.append("")
        bacholer.append("")
        asso.append("")
        llm.append("")
    elif "Associate" in i:
        asso.append("Associate")
        master.append("")
        bacholer.append("")
        gc.append("")
        llm.append("")
    elif "LLM" in i or "LL.M." in i or "LL.M" in i:
        llm.append("LLM")
        master.append("")
        bacholer.append("")
        gc.append("")
        asso.append("")
    else:
        master.append("")
        bacholer.append("")
        gc.append("")
        asso.append("")
        llm.append("")
    



```


```python
list1["Master"]=master
list1["Bacholer"]=bacholer
list1["Graduate Certificate"]=gc
list1["Associate"]=asso
list1["LLM"]=llm
```


```python
list1.to_csv(r'C:\Users\user\Downloads\unirank1.csv')
```
