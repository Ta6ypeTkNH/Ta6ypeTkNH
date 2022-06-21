import pyttsx3

while True:
    Question = input("Введите текст:")
    if Question == "Таров":
        engine = pyttsx3.init()
        engine.say("Таров")
        engine.runAndWait()
    elif Question == "Ты как?":
        engine = pyttsx3.init()
        engine.say("Да нормально")
        engine.runAndWait()
    elif Question == "Ты робот?":
        engine = pyttsx3.init()
        engine.say("Всмысле")
        engine.runAndWait()
    elif Question == "Пока":
        engine = pyttsx3.init()
        engine.say("Пока")
        engine.runAndWait()
    elif Question == "Как тебя зовут?":
        engine = pyttsx3.init()
        engine.say("Не обязана")
        engine.runAndWait()
    else:
        engine = pyttsx3.init()
        engine.say("Ты че, упал на клавиатуру?")
        engine.runAndWait()



import telebot
# Создаем экземпляр бота
bot = telebot.TeleBot('5468489458:AAHyRyPaeEL01MlVZKEL_X-SWSCOqF6qQlY')
# Функция, обрабатывающая команду /start
@bot.message_handler(commands=["start"])
def start(m, res=False):
    bot.send_message(m.chat.id, 'Я на связи. Напиши мне что-нибудь )')
# Получение сообщений от юзера
@bot.message_handler(content_types=["text"])
def handle_text(message):
    if message.text == "Таров":
        bot.send_message(message.chat.id, 'Тарова чертила')
    elif message.text == "Как дела?":
        bot.send_message(message.chat.id, 'Лучше чем у тебя')
    elif message.text == "Че такой злой?":
        bot.send_message(message.chat.id, 'А че бы и нет')
    else:
        bot.send_message(message.chat.id, 'Умер, помянем')
# Запускаем бота
bot.polling(none_stop=True, interval=0)
