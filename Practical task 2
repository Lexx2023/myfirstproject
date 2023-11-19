import pandas as pd
from sklearn. preprocessing import OneHotEncoder
moi_dan1 = pd.read_csv('New_DATA_1.csv') # чтение данных в переменную moi_dan1. Взят отчет (частично) о курьерских отправлениях контрагентам компании
df1 = pd.DataFrame(moi_dan1) # создание датафрейма "df1" из переменной moi_dan1
# print(df1) # вывод всего датафрейма "df1"
print()
str1 = df1.to_string()
print(str1)
print()
print (df1.info()) # вывод информации о датафрейме "df1": кол-во строк, кол-во столбцов, типах данных
print()
print('Количество строк/столбцов фрейма ',df1.shape)
print(df1.columns)
print(df1.describe())
print()
#создание экземпляра one-hot-encoder
encoder = OneHotEncoder(handle_unknown='ignore')
#выполнение горячего кодирование столбца 'Наименование городов'
encoder_df1 = pd.DataFrame(encoder. fit_transform(df1[['Наименование городов']]). toarray ())
# объединение столбца горячего кодирования с исходным DataFrame df1
final_df1 = df1.join (encoder_df1)
# print(final_df1)
str2 = final_df1.to_string()
print()
print(str2)
