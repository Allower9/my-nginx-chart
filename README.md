

#### 1)Создаём структуру
`
helm create my-nginx-chart `

#### 2)меняем все под себя, добавляем наши templates 

#### 3) Линтирование ==> Проверяем helm lint <путь-до-чарта/my-nginx-chart>  (1 chart(s) linted, 0 chart(s) failed ) ==> норма

#### 4)  Темплейтирование
   `helm template my-nginx-chart/ `

#### 5) Dry run
   `helm install my-release my-nginx-chart/ --dry-run`



#### 6) Установите чарт со значениями по умолчанию
   `cd /Users/allower`
   `helm install my-release my-nginx-chart -n web-app --create-namespace `

#### все четко 𓆏 
<img width="2064" height="966" alt="image" src="https://github.com/user-attachments/assets/c0ee40fd-9bf4-4720-b6a4-33839c606b77" />


#### 7) пробуем не стоковые values (создал custom-values.yaml) - там другая страничка index.html 
`cd /Users/allower`
`helm upgrade my-release my-nginx-chart -n web-app -f custom-values.yaml`
<img width="2750" height="1720" alt="image" src="https://github.com/user-attachments/assets/6e9e5755-f83b-4709-9d10-bcbad5b1c620" />

#### 8) Удаляем
<img width="2828" height="488" alt="image" src="https://github.com/user-attachments/assets/6a81651f-f423-4063-94d3-5174337013a8" />
