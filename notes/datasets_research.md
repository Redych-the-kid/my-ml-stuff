# **Практика: поиск датасета**
Я нашёл нормальное пояснение для датасета вот здесь, но я не уверен, на английском ли он(проверю чуть позже после расписания всех датасетов, предоставленных по ссылке)
https://arxiv.org/abs/2401.02034 (Ссылка на статью с ссылкой на датасеты)


## Датасет 
**Ссылка на датасет** : https://tianchi.aliyun.com/dataset/95414
Тут есть несколько датасетов, но я без понятия, какой подходит под нашу задачу. Вроде бы есть парочка, но они не совсем "полные", или мне так кажется, я не пойму. В общем...

## Как я понял датасеты и их содержание:
**Chinese Medical Named Entity Recognition Dataset (CMeEE)** - на вход получаем предложение по типу:
```
Complications including pneumonia and atelectasis can be developed in patients with respiratory muscle paralysis or respiratory center involvement due to difficult breathing.
```
А на выходе мы получаем список сущностей с их классами. Классов может быть 9:
* `dis` - болезнь
* `sym` - симптом
* `dru` - лекарства
* `equ` - медоборудование
* `pro` - процедура
* `bod` - часть тела
* `ite` - предметы медобследования
* `mic` - микроорганизмы
* `dep` - отделение
**Chinese Medical Information Extraction Dataset (CMeIE)** -  превращает предложения в триплеты. Но судя по всему это не те триплеты, что нам нужны в задаче:
``` json
English:
{  
  "text": "Chronic pancreatitis@ ###low-dosage radiation Since 1964, there have been serial reports on cases that external radiation (5-50Gy) can relieve pains in patients with chronic pancreatitis. Chronic pancreatitis@ Conceptually, external radiation has anti-inflammatory and analgesic effects, and it has already been used for non-tumor pain relief.", 
  "spo_list": [ 
    { 
      "predicate": "Radiation Therapy", 
      "subject": "chronic pancreatitis", 
      "subject_type": "Disease", 
      "object": { "@value": "external radiation" }, 
      "object_type": { "@value": "Other Therapy" } 
    }, 
    { 
      "predicate": "Radiation Therapy", 
      "subject": "non-tumor pain", 
      "subject_type": "Disease", 
      "object": { "@value": "external radiation" }, 
      "object_type": { "@value": "Other Therapy" } 
      }
    }
  ] 
}
```
Остальные датасеты - либо про книги, либо уже про вопрос-ответ, вопрос-вопрос и тд.
## Вопросы
- [ ] Какой датасет изучить?
- [ ] Как его запихать в модель?
- [ ] Что почитать/посмотреть по этому всему?
