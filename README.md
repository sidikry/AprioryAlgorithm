CONTOH PENERAPAN ALGORITMA APRIORI

CARA PENGGUNAAN :

PANDUAN PENGGUNAAN
-Install anaconda python 3.7 https://www.anaconda.com/distribution/
-Buka Spyder pada Anaconda Navigator -> pilih base(root)
-Simpan hasil clone/unduh ini di dalam partisi C:/
-Buka Pada File Explorer di Spyder

IKUTI LANGKAH SATU PER SATU

# Impor Libary Dibawah dengan Ctrl + Enter
# Importing the libraries
import numpy as np
import matplotlib.pyplot as plt
import pandas as pd

#Import dataset dengan perintah dibawah dengan Ctrl + Enter
# Data Preprocessing
dataset = pd.read_csv('Market_Basket_Optimisation.csv', header = None)

#Jalankan Perintah dibawah ini lalu Ctrl + Enter
transactions = []
for i in range(0, 7501):
    transactions.append([str(dataset.values[i,j]) for j in range(0, 20)])
	
#Training The Dataset jalankan perintah dibawah dengan Ctrl + Enter
from apyori import apriori
rules = apriori(transactions, min_support = 0.003, min_confidence = 0.2, min_lift = 3, min_length = 2)

#Lihat hasil Frequent Set-Item -> Jalankan Perintah dibawah dengan Ctrl + Enter
results = list(rules)

#Apabila tidak support Frozenset maka gunakan perintah dibawah
for i in results:
    print(i)
    print('**********')
	
	######################## GOOD LUCK ##################################





