
<img src="img/DbUrOkwbbbk (1).jpg" height="400px" border="5px solid red" />



# Artem Rubchenko
-----
# Beginner Frontend Developer
-------
# My contacts:

* **Address:** Vitebsk, st. Shmyreva, 8, Republic of Belarus
* **My contact phone:** +375292146599
* **E-mail:** [rubchenko1994@gmail.com](https://mail.google.com/mail/u/0/)
* **LinkedIn:** [Artem Rubchenko](https://www.linkedin.com/in/artem-rubchenko-984b6a169/)
* **GitHub:** [RubchenkoArtem](https://github.com/RubchenkoArtem)
* **CodePen:** [RubchenkoArtem](https://codepen.io/RubchenkoArtem)
* **Medium:** [rubchenko](https://medium.com/@rubchenko1994)
* **Discord:** [BlackWalker94#8514](BlackWalker94#8514)
* **Telegram:** [@blackwalker94](https://t.me/blackwalker94)
* **Vkontakte:** [BlackWalker94](https://vk.com/blackwalker94)
* **Twitter:** [@94blackwalker](https://twitter.com/94Blackwalker)
* **Youtube channel:** [BlackWalker94](https://www.youtube.com/channel/UCkAZEOYHvFxaI_Bz9OodhOg) 
* **Twich channel:** [blackwalker94](https://www.twitch.tv/blackwalker94)
* **Steam:** [blackwalker94](https://steamcommunity.com/profiles/76561198096157874/)

-----

# Summary

 Beginner Frontend Developer with no work experience, but with a great desire to learn and discover a new stage in life.

-------

# Skills

* Basic HTML$CSS 
* Basic JavaScript
* 3D modeling, design.
* * C (basic), Python(basic), SQLite(basic).
* Windows OS, Linux(Ubuntu)
* * Editors: **VSCode**, PyCharm community, Blender.

------

# Code examples

```Python
bot = Bot(token=tg_bot_token)
dp = Dispatcher(bot)


@dp.message_handler(commands=["start"])
async def start_command(message: types.Message):
    await message.reply("Привет! Напиши мне название города и я пришлю сводку погоды!")


@dp.message_handler()
async def get_weather(message: types.Message):
    code_to_smile = {
        "Clear": "Ясно \U00002600",
        "Clouds": "Облачно \U00002601",
        "Rain": "Дождь \U00002614",
        "Drizzle": "Дождь \U00002614",
        "Thindersorm": "Гроза \U000026A1",
        "Snow": "Снег \U0001F328",
        "Mist": "Туман \U0001F328"
    }
   
    try:
        r = requests.get(
            f"https://api.openweathermap.org/data/2.5/weather?q={message.text}&appid={open_weather_token}&units=metric"
        )
        data = r.json()
        
        city = data["name"]
        cur_weather = data["main"]["temp"]

        weather_description = data['weather'][0]['main']
        if weather_description in code_to_smile:
            wd = code_to_smile[weather_description]
        else:
            wd = "Посмотри в окно, не пойму что там за погода!"

        humidity = data['main']['humidity']
        pressure = data['main']['pressure']
        wind = data['wind']['speed']
        sunrise_timestamp = datetime.datetime.fromtimestamp(data['sys']['sunrise'])
        sunset_timestamp = datetime.datetime.fromtimestamp(data['sys']['sunset'])
        length_of_the_day = datetime.datetime.fromtimestamp(data['sys']['sunset']) - datetime.datetime.fromtimestamp(data['sys']['sunrise']) 

        await message.reply(f"***{datetime.datetime.now().strftime('%Y-%m-%d-%H:%M')}***\n"
              f"Погода в городе: {city}\nТемпература: {cur_weather} С° {wd}\n"
              f"Влажность: {humidity}\nДавление: {pressure} мм.рт.ст.\nВетер: {wind} м/с\n"
              f"Восход солнца: {sunrise_timestamp}\nЗакат солнца: {sunset_timestamp}\nПродолжительность дня: {length_of_the_day}\n"
              f"***Хорошего дня!***"
              )


    except:
       await message.reply("\U00002620 Проверьте название города \U00002620")

if __name__ == '__main__' :  
    executor.start_polling(dp)
```
-------

# Education

* **Higher Educational Institution "Vitebsk State Technological University"**
    * Faculty of Information Technology and Robotics.
    * Specialization: process automation engineer (light industry)
* **Vitebsk branch of the International University “MITSO”**
    * faculty of jurisprudence.
    * specialization: lawyer.

-----

# Experience

* I have little experience in JS and Frontend, but I have a great desire to learn and gain the necessary experience.

----

# Languages

- Belarussian
- Russian
- English (Starter A1)
----

> **_Words that influenced me:_**
>* _"The biggest risk is not to take risks. In a rapidly changing world, this is the only tactic that is guaranteed to lead to failure." - Mark Zuckerberg (Co-founder of Facebook*)_ 
>* _"If you start doing something new, be prepared to be misunderstood. - Jeff Bezos (The founder of Amazon.)"_
>* _"Just work like hell. If others work 40 hours a week, and you work 100 hours, then even doing the same, you will be able to achieve results two and a half times faster. What others will need a year to do, you will be able to do in four months. And if you're lazy, just don't waste time trying to launch your business. - Elon Musk (Engineer, inventor, co-founder of PayPal, SpaceX, Tesla.)"_
>* _"You can't go through life without failing at least in some way. And if you live carefully, constantly afraid of failure, you fail by default. - Joanne Rowling (Author of the Harry Potter series of novels.)- "_


