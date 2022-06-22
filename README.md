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
from telebot import types
# Создаем экземпляр бота
bot = telebot.TeleBot('5468489458:AAHyRyPaeEL01MlVZKEL_X-SWSCOqF6qQlY')
# Функция, обрабатывающая команду /start
@bot.message_handler(commands=["start"])
def handle_text(message):
    keyboard = types.InlineKeyboardMarkup();  # наша клавиатура
    key_citi1 = types.InlineKeyboardButton(text='Челябинск', callback_data='citi1');  # кнопка «Да»
    keyboard.add(key_citi1);  # добавляем кнопку в клавиатуру
    key_city2 = types.InlineKeyboardButton(text='Санкт-Петербург', callback_data='city2');
    keyboard.add(key_city2);
    key_city3 = types.InlineKeyboardButton(text='Москва', callback_data='city3');
    keyboard.add(key_city3)
    bot.send_message(message.from_user.id,'Привет! Я твой бот-гид Njmu, пожалуйста выбери город в котором хочешь найти интересные места.', reply_markup=keyboard)
    @bot.callback_query_handler(func=lambda call: True)
    def callback_worker(call):
        if call.data == "citi1":
            keyboard = types.InlineKeyboardMarkup();  # наша клавиатура
            key_citi1 = types.InlineKeyboardButton(text='Центральный', callback_data='citi1');  # кнопка «Да»
            keyboard.add(key_citi1);  # добавляем кнопку в клавиатуру
            key_city2 = types.InlineKeyboardButton(text='Северо-Западный', callback_data='city2');
            keyboard.add(key_city2);
            key_city3 = types.InlineKeyboardButton(text='Ленинский', callback_data='city3');
            keyboard.add(key_city3)
            bot.send_message(call.message.chat.id, 'Вот весь список Районов в этом городе:', reply_markup=keyboard)
        elif call.data == "city2":
            bot.send_message(call.message.chat.id, '2');
        elif call.data == 'city3':
            bot.send_message(call.message.chat.id, '3');
# Запускаем бота
bot.polling(none_stop=True, interval=0)
