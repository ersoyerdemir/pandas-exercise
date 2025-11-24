import numpy as np

import pandas as pd
### Aşağıdaki sözlükten bir DataFrame oluştur:
"""data = {
    "Ad":["Ali","Ayşe","Mehmet","Zeynep"],
    "Yaş":[20,25,22,30],
    "Şehir":["İzmir","Ankara","İstanbul","Bursa"]
}

df = pd.DataFrame(data)

print(df)
print("-------------------------------")

print(df.info)
print ("-------------------------------")

print (df.describe)
print ("-------------------------------")
###S2 — Sadece “Ad” ve “Şehir” sütunlarını seçme
print(df[["Ad", "Şehir"]])
print ("-------------------------------")
###S3 — Yaşı 23’ten büyük olanları filtreleme
print(df[df["Yaş"] > 23])
print ("-------------------------------")
###S4 — Yeni sütun ekleme
df["Mezun"] = [True, True, False, True]
print(df)
print ("-------------------------------")
###S5 — Yaş ortalaması

print(df["Yaş"].mean())"""





data ={
    "İsim":["Eren","Merve","Hasan","Elif","Deniz"],
    "Not":[75, 88, 92, 60, 85],
    "Bölüm":["Yazılım","İşletme","Yazılım","Endüstri","İşletme"],
    "Yaş":[21, 24, 23, 27, 22]
    }


df= pd.DataFrame(data)

print(df)
print("-------------------------")
print(df[["İsim","Bölüm"]])
print("-------------------------")
print(df[df["Not"]>80])
print("-------------------------")
t =df.sort_values("Yaş")
print(t)
print("-------------------------")
k =df["Geçti"] = df["Not"] >= 70
print(k)
print("-------------------------")
o=df.groupby("Bölüm")["Not"].mean()
"""
burada bölümlere göre not ortalamalarını filtreliyoruz bunu yaparken yapıcamız işlemi bi değere eşitlersek print ile ekrana yazdırırken daha az kafamız karşır 
df.gruopby dedikten sonra hangi koşula göreyse onu () parantezine alırken o koşula göre neyi istiyosak [] parantezine alıp sonrasında ortalama bulmaya yarayan method olan 
.mean methoduyla bağlıyoruz 

sonuç olarak üniversitenin bölümlerine göre not ortalamalarını ekrana yazdırdık 

"""


print(o)
print("-------------------------")

df.nlargest(3, "Not")
a= df.sort_values("Not", ascending=False).head(3)
print(a)
pandas kütüphanesinde başlangıç kısmı için bir çalışma gerçekleştirdim umarım faydalı olur
