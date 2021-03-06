## label

В примере у нас есть текстовое поле **race**. Но нигде не указано подсказки, что это за поле. 
Пользователь просто не поймет, что все это значит.

Для добавления надписи мы можем воспользоваться тегом `label`. 
Дополнительно сгруппируем их с помощью тега `fieldset` и добавим группе название `legend`.

```html
<form action="/example" method="GET">
   <h6>Наша первая форма</h6> 
   <fieldset>
       <legend>Основная информация</legend>
       <input type="text" name="username" placeholder="Введите свое имя"/>
       <hr />
       <input type="number" name="phone" placeholder="Введите свой номер телефона"/>
   </fieldset>
   <fieldset>
      <label for="race">Введите свою расу</label>
      <input type="text" id="race" name="race" value="Человек"/>
   </fieldset>
</form>
```

Результат:

<div class="html">
    <form action="/example" method="GET">
       <h6>Наша первая форма</h6> 
       <fieldset>
           <legend>Основная информация</legend>
           <input class="form-control" type="text" name="username" placeholder="Введите свое имя"/>
           <hr />
           <input class="form-control" type="number" name="phone" placeholder="Введите свой номер телефона"/>
       </fieldset>
       <fieldset>
          <label for="race">Введите свою расу</label>
          <input class="form-control" type="text" id="race" name="race" value="Человек"/>
       </fieldset>
    </form>
</div>

Атрибут `for` указывает к какому `input` привязана данная надпись по `id`.

### Задание

Добавьте лейблы для каждого поля в нашей форме. Не забудьте привязать его с помощью `id` и `for`.