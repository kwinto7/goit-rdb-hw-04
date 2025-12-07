# goit-rdb-hw-04
<img width="196" height="240" alt="image" src="https://github.com/user-attachments/assets/a03986d7-98da-4222-b281-65321cb75360" />
<img width="480" height="676" alt="image" src="https://github.com/user-attachments/assets/1feb7bac-e549-4766-9eb6-905b95099f2d" />
<img width="1215" height="202" alt="image" src="https://github.com/user-attachments/assets/7f6795cd-12ef-41ce-9d8b-a23edf06030e" />
<br>
<img width="548" height="57" alt="image" src="https://github.com/user-attachments/assets/95683802-8cf2-4d45-a99e-2e287bbfc674" />
<img width="191" height="87" alt="image" src="https://github.com/user-attachments/assets/c2d01dbb-addc-4ba2-87b6-05d43763f0c7" />  
<br>
<img width="446" height="42" alt="image" src="https://github.com/user-attachments/assets/80483fdd-f457-480d-afa4-5421fd4d4553" />
<img width="176" height="82" alt="image" src="https://github.com/user-attachments/assets/df346e90-4e1b-447e-92bc-8b9679690b68" />  
<br>
<img width="811" height="44" alt="image" src="https://github.com/user-attachments/assets/b2fc4b4e-9994-4293-aacd-f9db9c40d903" />
<img width="427" height="70" alt="image" src="https://github.com/user-attachments/assets/8d94ed2a-518a-4883-9cb1-a9cf2bdda4f4" />  
<br>
<img width="570" height="47" alt="image" src="https://github.com/user-attachments/assets/66202ab6-ca2e-47aa-995b-a60aae433110" />
<img width="272" height="82" alt="image" src="https://github.com/user-attachments/assets/ca5e73f2-06fe-42e7-961d-56aa11dca5fc" />  
<br>
<img width="839" height="55" alt="image" src="https://github.com/user-attachments/assets/fe2abd33-6fcd-418b-8b4d-d0bdd12b63cf" />
<img width="361" height="85" alt="image" src="https://github.com/user-attachments/assets/54c3b974-9646-4446-98df-475f4415d5f9" />  
<br>
<img width="516" height="203" alt="image" src="https://github.com/user-attachments/assets/7154ead0-bce1-4282-8b79-011388d0e712" />  
<img width="3075" height="507" alt="image" src="https://github.com/user-attachments/assets/e554c10d-b9ce-4126-a1c6-4bb9881b7718" />
<br>
<img width="512" height="197" alt="image" src="https://github.com/user-attachments/assets/2bb4bb68-d3f7-483b-b8cc-4a2f79e71055" />
<img width="123" height="57" alt="image" src="https://github.com/user-attachments/assets/7b4e9c85-0507-4e11-8a83-12507aec1af8" />

Після заміни деяких операторів INNER JOIN на LEFT JOIN кількість рядків у результаті залишається такою самою.

Причина в тому, що:

- INNER JOIN повертає тільки ті рядки, для яких у обох таблицях є відповідні записи згідно з умовою ON. Якщо для певного запису з лівої таблиці немає відповідного запису в правій, цей рядок повністю відкидається з результату.

- LEFT JOIN повертає всі рядки з лівої таблиці незалежно від того, чи знайдено відповідний запис у правій таблиці. Якщо відповідного запису немає, поля правої таблиці заповнюються значеннями NULL.

Отже:
- кількість рядків при LEFT JOIN не може бути меншою, ніж при INNER JOIN;
- якщо всі зовнішні ключі коректні (для кожного order_details існує order, для кожного order існує customer тощо), то кількість рядків з INNER JOIN і LEFT JOIN буде однаковою;
- якщо є "висячі" записи (наприклад, у order_details є order_id, якого немає в таблиці orders), то при INNER JOIN ці рядки відкидаються, а при LEFT JOIN вони залишаються з NULL у полях приєднаної таблиці, тому кількість рядків зростає.

RIGHT JOIN працює аналогічно LEFT JOIN, але "з точністю навпаки": гарантовано зберігаються всі рядки з правої таблиці, а для відсутніх відповідників у лівій таблиці підставляються NULL.
<br>
<img width="512" height="239" alt="image" src="https://github.com/user-attachments/assets/3950d044-c0c5-4096-bfd7-90273db3d3dc" />
<img width="1039" height="22" alt="image" src="https://github.com/user-attachments/assets/c71db813-4afb-4042-91ed-ca55e8e51d35" />
<br>
<img width="299" height="223" alt="image" src="https://github.com/user-attachments/assets/e68dc5a9-9d9f-416c-9b23-f8fd07fa94ac" />
<img width="285" height="173" alt="image" src="https://github.com/user-attachments/assets/17db070d-c302-4fd9-ac68-bdedb84abaa8" />
<br>





