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
    keyboard = types.InlineKeyboardMarkup()  # наша клавиатура
    key_city1 = types.InlineKeyboardButton(text='Челябинск', callback_data='city1')  # кнопка «Да»
    keyboard.add(key_city1)  # добавляем кнопку в клавиатуру
    key_city2 = types.InlineKeyboardButton(text='Санкт-Петербург', callback_data='city2')
    keyboard.add(key_city2)
    key_city3 = types.InlineKeyboardButton(text='Москва', callback_data='city3')
    keyboard.add(key_city3)
    key_city4 = types.InlineKeyboardButton(text='Екантеринбург', callback_data='city4')
    keyboard.add(key_city4)
    key_city5 = types.InlineKeyboardButton(text='Новосибирск', callback_data='city5')
    keyboard.add(key_city5)
    bot.send_message(message.from_user.id,'Привет! Я твой бот-гид Njmu, пожалуйста выбери город в котором хочешь найти интересные места.', reply_markup=keyboard)
    @bot.callback_query_handler(func=lambda call: True)
    def callback_worker(call):
        if call.data == "city1":
            keyboard = types.InlineKeyboardMarkup()  # наша клавиатура
            key_city1 = types.InlineKeyboardButton(text='Центральный', callback_data='city13')  # кнопка «Да»
            keyboard.add(key_city1)  # добавляем кнопку в клавиатуру
            key_city2 = types.InlineKeyboardButton(text='Металлургический', callback_data='city12')
            keyboard.add(key_city2)
            key_city3 = types.InlineKeyboardButton(text='Ленинский', callback_data='city11')
            keyboard.add(key_city3)
            key_city4 = types.InlineKeyboardButton(text='Советский', callback_data='city4')
            keyboard.add(key_city4)
            key_city5 = types.InlineKeyboardButton(text='Тракторозаводский', callback_data='city5')
            keyboard.add(key_city5)
            key_city6 = types.InlineKeyboardButton(text='Курчатовский', callback_data='city6')
            keyboard.add(key_city6)
            key_city7 = types.InlineKeyboardButton(text='Калининский', callback_data='city7')
            keyboard.add(key_city7)
            bot.send_message(call.message.chat.id, 'Вот весь список Районов в этом городе:', reply_markup=keyboard)
        if call.data == "city2":
            keyboard = types.InlineKeyboardMarkup()  # наша клавиатура
            key_city1 = types.InlineKeyboardButton(text='Невский', callback_data='city8')  # кнопка «Да»
            keyboard.add(key_city1)  # добавляем кнопку в клавиатуру
            key_city2 = types.InlineKeyboardButton(text='Калининский', callback_data='city9')
            keyboard.add(key_city2)
            key_city3 = types.InlineKeyboardButton(text='Курортный', callback_data='city10')
            keyboard.add(key_city3)
            key_city4 = types.InlineKeyboardButton(text='Адмиралтейский', callback_data='city4')
            keyboard.add(key_city4)
            key_city5 = types.InlineKeyboardButton(text='Василеостровский', callback_data='city5')
            keyboard.add(key_city5)
            key_city6 = types.InlineKeyboardButton(text='Выборгский', callback_data='city6')
            keyboard.add(key_city6)
            key_city7 = types.InlineKeyboardButton(text='Кировский', callback_data='city7')
            keyboard.add(key_city7)
            key_city8 = types.InlineKeyboardButton(text='Колпинский', callback_data='city8')
            keyboard.add(key_city8)
            key_city9 = types.InlineKeyboardButton(text='Красногвардейский', callback_data='city9')
            keyboard.add(key_city9)
            key_city10 = types.InlineKeyboardButton(text='Красносельский', callback_data='city10')
            keyboard.add(key_city10)
            key_city11 = types.InlineKeyboardButton(text='Кронштадтcкий', callback_data='city11')
            keyboard.add(key_city11)
            key_city12 = types.InlineKeyboardButton(text='Московский', callback_data='city12')
            keyboard.add(key_city12)
            key_city13 = types.InlineKeyboardButton(text='Петроградский', callback_data='city13')
            keyboard.add(key_city13)
            key_city14 = types.InlineKeyboardButton(text='Петродворцовый', callback_data='city14')
            keyboard.add(key_city14)
            key_city15 = types.InlineKeyboardButton(text='Приморский', callback_data='city15')
            keyboard.add(key_city15)
            key_city16 = types.InlineKeyboardButton(text='Пушкинский', callback_data='city16')
            keyboard.add(key_city16)
            key_city17 = types.InlineKeyboardButton(text='Фрунзенский', callback_data='city17')
            keyboard.add(key_city17)
            key_city18 = types.InlineKeyboardButton(text='Центральный', callback_data='city18')
            keyboard.add(key_city18)
            bot.send_message(call.message.chat.id, 'Вот весь список Районов в этом городе:', reply_markup=keyboard)
        if call.data == 'city3':
            keyboard = types.InlineKeyboardMarkup()  # наша клавиатура
            key_city1 = types.InlineKeyboardButton(text='Центр', callback_data='city5')  # кнопка «Да»
            keyboard.add(key_city1)  # добавляем кнопку в клавиатуру
            key_city2 = types.InlineKeyboardButton(text='Останкино', callback_data='city6')
            keyboard.add(key_city2)
            key_city3 = types.InlineKeyboardButton(text='Дмитровка', callback_data='city7')
            keyboard.add(key_city3)
            key_city4 = types.InlineKeyboardButton(text='Медведково', callback_data='city4')
            keyboard.add(key_city4)
            key_city5 = types.InlineKeyboardButton(text='Ховрино', callback_data='city5')
            keyboard.add(key_city5)
            key_city6 = types.InlineKeyboardButton(text='Тушино', callback_data='city6')
            keyboard.add(key_city6)
            key_city7 = types.InlineKeyboardButton(text='Митино', callback_data='city7')
            keyboard.add(key_city7)
            key_city8 = types.InlineKeyboardButton(text='Строгино', callback_data='city8')
            keyboard.add(key_city8)
            key_city9 = types.InlineKeyboardButton(text='Хорошево', callback_data='city9')
            keyboard.add(key_city9)
            key_city10 = types.InlineKeyboardButton(text='Фили', callback_data='city10')
            keyboard.add(key_city10)
            key_city11 = types.InlineKeyboardButton(text='Юго-Запад', callback_data='city11')
            keyboard.add(key_city11)
            key_city12 = types.InlineKeyboardButton(text='Бутово', callback_data='city12')
            keyboard.add(key_city12)
            key_city13 = types.InlineKeyboardButton(text='Каширка', callback_data='city13')
            keyboard.add(key_city13)
            key_city14 = types.InlineKeyboardButton(text='Зябликово', callback_data='city14')
            keyboard.add(key_city14)
            key_city15 = types.InlineKeyboardButton(text='Сукино болото', callback_data='city15')
            keyboard.add(key_city15)
            key_city16 = types.InlineKeyboardButton(text='Люблино', callback_data='city16')
            keyboard.add(key_city16)
            key_city17 = types.InlineKeyboardButton(text='Жулебино', callback_data='city17')
            keyboard.add(key_city17)
            key_city18 = types.InlineKeyboardButton(text='Кузьминки', callback_data='city18')
            keyboard.add(key_city18)
            key_city19 = types.InlineKeyboardButton(text='Вешняки', callback_data='city19')
            keyboard.add(key_city19)
            key_city20 = types.InlineKeyboardButton(text='Перово', callback_data='city20')
            keyboard.add(key_city20)
            key_city21 = types.InlineKeyboardButton(text='Лефортово', callback_data='city21')
            keyboard.add(key_city21)
            key_city22 = types.InlineKeyboardButton(text='Измайлово', callback_data='city22')
            keyboard.add(key_city22)
            bot.send_message(call.message.chat.id, 'Вот весь список Районов в этом городе:', reply_markup=keyboard)
        if call.data == "city4":
            keyboard = types.InlineKeyboardMarkup()  # наша клавиатура
            key_city1 = types.InlineKeyboardButton(text='Чкаловский', callback_data='city14')  # кнопка «Да»
            keyboard.add(key_city1)  # добавляем кнопку в клавиатуру
            key_city2 = types.InlineKeyboardButton(text='Кировский', callback_data='city15')
            keyboard.add(key_city2)
            key_city3 = types.InlineKeyboardButton(text='Ленинский', callback_data='city16')
            keyboard.add(key_city3)
            key_city4 = types.InlineKeyboardButton(text='Октябрьский', callback_data='city4')
            keyboard.add(key_city4)
            key_city5 = types.InlineKeyboardButton(text='Орджоникидзевский', callback_data='city5')
            keyboard.add(key_city5)
            key_city6 = types.InlineKeyboardButton(text='Железнодорожный', callback_data='city6')
            keyboard.add(key_city6)
            key_city7 = types.InlineKeyboardButton(text='Верх-Исетский', callback_data='city7')
            keyboard.add(key_city7)
            bot.send_message(call.message.chat.id, 'Вот весь список Районов в этом городе:', reply_markup=keyboard)
        if call.data == "city5":
            keyboard = types.InlineKeyboardMarkup()  # наша клавиатура
            key_city1 = types.InlineKeyboardButton(text='Дзержинский', callback_data='city17')  # кнопка «Да»
            keyboard.add(key_city1)  # добавляем кнопку в клавиатуру
            key_city2 = types.InlineKeyboardButton(text='Первомайский', callback_data='city18')
            keyboard.add(key_city2)
            key_city3 = types.InlineKeyboardButton(text='Октябрьский', callback_data='city19')
            keyboard.add(key_city3)
            key_city4 = types.InlineKeyboardButton(text='Железнодорожный', callback_data='city4')
            keyboard.add(key_city4)
            key_city5 = types.InlineKeyboardButton(text='Заельцовский', callback_data='city5')
            keyboard.add(key_city5)
            key_city6 = types.InlineKeyboardButton(text='Калининский', callback_data='city6')
            keyboard.add(key_city6)
            key_city7 = types.InlineKeyboardButton(text='Кировский', callback_data='city7')
            keyboard.add(key_city7)
            key_city8 = types.InlineKeyboardButton(text='Советский', callback_data='city8')
            keyboard.add(key_city8)
            key_city9 = types.InlineKeyboardButton(text='Центральный', callback_data='city9')
            keyboard.add(key_city9)
            key_city10 = types.InlineKeyboardButton(text='Ленинский', callback_data='cit10')
            keyboard.add(key_city10)
            bot.send_message(call.message.chat.id, 'Вот весь список Районов в этом городе:', reply_markup=keyboard)
        if call.data == 'city6':
            keyboard = types.InlineKeyboardMarkup()  # наша клавиатура
            key_city1 = types.InlineKeyboardButton(text='Военно-патриотические - это все объекты с военными действиями.', callback_data='city1')  # кнопка «Да»
            keyboard.add(key_city1)  # добавляем кнопку в клавиатуру
            key_city2 = types.InlineKeyboardButton(text='Культурные объекты - театры, концертные залы, кинотеатры - всё, что связано с искусством.', callback_data='city2')
            keyboard.add(key_city2)
            key_city3 = types.InlineKeyboardButton(text='Развлекательные объекты - казино, боулинг, караоке', callback_data='city3')
            keyboard.add(key_city3)
            key_city4 = types.InlineKeyboardButton(text='Религиозные объекты - церкви, костелы, кирхи, синагоги, капища, языческие идолы и валуны', callback_data='city4')
            keyboard.add(key_city4)
            key_city5 = types.InlineKeyboardButton(text='Исторические объекты - для это все достопримечательности, которые старше ста лет.', callback_data='city5')
            keyboard.add(key_city5)
            key_city6 = types.InlineKeyboardButton(text='Архитектурные объекты - здания, скульптурные композиции, фонтаны.', callback_data='city6')
            keyboard.add(key_city6)
            key_city7 = types.InlineKeyboardButton(text='Природные объекты - национальные парки, заповедники, зоопарки, гейзеры, водоемы - сюда же относится пляжный отдых и рыбалка.', callback_data='city7')
            keyboard.add(key_city7)
            key_city8 = types.InlineKeyboardButton(text='Общепит - так же может быть достопримечательностью: рестораны, кафе, пабы, бары.', callback_data='city8')
            keyboard.add(key_city8)
            key_city9 = types.InlineKeyboardButton(text='Достопримечательности для детей: аквапарки, детские городки, цирк и тому подобное - то же условно, потому, как аквапарки, зоопарки и цирк интересны не только детям, но и взрослым.', callback_data='city9')
            keyboard.add(key_city9)
            bot.send_message(call.message.chat.id, 'Выберите нужную для вас достопримечательность:',reply_markup=keyboard)
        if call.data == 'city7':
            keyboard = types.InlineKeyboardMarkup()  # наша клавиатура
            key_city1 = types.InlineKeyboardButton(text='Военно-патриотические - это все объекты с военными действиями.', callback_data='city1')  # кнопка «Да»
            keyboard.add(key_city1)  # добавляем кнопку в клавиатуру
            key_city2 = types.InlineKeyboardButton(text='Культурные объекты - театры, концертные залы, кинотеатры - всё, что связано с искусством.', callback_data='city2')
            keyboard.add(key_city2)
            key_city3 = types.InlineKeyboardButton(text='Развлекательные объекты - казино, боулинг, караоке', callback_data='city3')
            keyboard.add(key_city3)
            key_city4 = types.InlineKeyboardButton(text='Религиозные объекты - церкви, костелы, кирхи, синагоги, капища, языческие идолы и валуны', callback_data='city4')
            keyboard.add(key_city4)
            key_city5 = types.InlineKeyboardButton(text='Исторические объекты - для это все достопримечательности, которые старше ста лет.', callback_data='city5')
            keyboard.add(key_city5)
            key_city6 = types.InlineKeyboardButton(text='Архитектурные объекты - здания, скульптурные композиции, фонтаны.', callback_data='city6')
            keyboard.add(key_city6)
            key_city7 = types.InlineKeyboardButton(text='Природные объекты - национальные парки, заповедники, зоопарки, гейзеры, водоемы - сюда же относится пляжный отдых и рыбалка.', callback_data='city7')
            keyboard.add(key_city7)
            key_city8 = types.InlineKeyboardButton(text='Общепит - так же может быть достопримечательностью: рестораны, кафе, пабы, бары.', callback_data='city8')
            keyboard.add(key_city8)
            key_city9 = types.InlineKeyboardButton(text='Достопримечательности для детей: аквапарки, детские городки, цирк и тому подобное - то же условно, потому, как аквапарки, зоопарки и цирк интересны не только детям, но и взрослым.', callback_data='city9')
            keyboard.add(key_city9)
            bot.send_message(call.message.chat.id, 'Выберите нужную для вас достопримечательность:', reply_markup=keyboard)
        if call.data == 'city8':
            keyboard = types.InlineKeyboardMarkup()  # наша клавиатура
            key_city1 = types.InlineKeyboardButton(text='Военно-патриотические - это все объекты с военными действиями.', callback_data='city1')  # кнопка «Да»
            keyboard.add(key_city1)  # добавляем кнопку в клавиатуру
            key_city2 = types.InlineKeyboardButton(text='Культурные объекты - театры, концертные залы, кинотеатры - всё, что связано с искусством.', callback_data='city2')
            keyboard.add(key_city2)
            key_city3 = types.InlineKeyboardButton(text='Развлекательные объекты - казино, боулинг, караоке', callback_data='city3')
            keyboard.add(key_city3)
            key_city4 = types.InlineKeyboardButton(text='Религиозные объекты - церкви, костелы, кирхи, синагоги, капища, языческие идолы и валуны', callback_data='city4')
            keyboard.add(key_city4)
            key_city5 = types.InlineKeyboardButton(text='Исторические объекты - для это все достопримечательности, которые старше ста лет.', callback_data='city5')
            keyboard.add(key_city5)
            key_city6 = types.InlineKeyboardButton(text='Архитектурные объекты - здания, скульптурные композиции, фонтаны.', callback_data='city6')
            keyboard.add(key_city6)
            key_city7 = types.InlineKeyboardButton(text='Природные объекты - национальные парки, заповедники, зоопарки, гейзеры, водоемы - сюда же относится пляжный отдых и рыбалка.', callback_data='city7')
            keyboard.add(key_city7)
            key_city8 = types.InlineKeyboardButton(text='Общепит - так же может быть достопримечательностью: рестораны, кафе, пабы, бары.', callback_data='city8')
            keyboard.add(key_city8)
            key_city9 = types.InlineKeyboardButton(text='Достопримечательности для детей: аквапарки, детские городки, цирк и тому подобное - то же условно, потому, как аквапарки, зоопарки и цирк интересны не только детям, но и взрослым.', callback_data='city9')
            keyboard.add(key_city9)
        if call.data == 'city9':
            keyboard = types.InlineKeyboardMarkup()  # наша клавиатура
            key_city1 = types.InlineKeyboardButton(text='Военно-патриотические - это все объекты с военными действиями.', callback_data='city1')  # кнопка «Да»
            keyboard.add(key_city1)  # добавляем кнопку в клавиатуру
            key_city2 = types.InlineKeyboardButton(text='Культурные объекты - театры, концертные залы, кинотеатры - всё, что связано с искусством.', callback_data='city2')
            keyboard.add(key_city2)
            key_city3 = types.InlineKeyboardButton(text='Развлекательные объекты - казино, боулинг, караоке', callback_data='city3')
            keyboard.add(key_city3)
            key_city4 = types.InlineKeyboardButton(text='Религиозные объекты - церкви, костелы, кирхи, синагоги, капища, языческие идолы и валуны', callback_data='city4')
            keyboard.add(key_city4)
            key_city5 = types.InlineKeyboardButton(text='Исторические объекты - для это все достопримечательности, которые старше ста лет.', callback_data='city5')
            keyboard.add(key_city5)
            key_city6 = types.InlineKeyboardButton(text='Архитектурные объекты - здания, скульптурные композиции, фонтаны.', callback_data='city6')
            keyboard.add(key_city6)
            key_city7 = types.InlineKeyboardButton(text='Природные объекты - национальные парки, заповедники, зоопарки, гейзеры, водоемы - сюда же относится пляжный отдых и рыбалка.', callback_data='city7')
            keyboard.add(key_city7)
            key_city8 = types.InlineKeyboardButton(text='Общепит - так же может быть достопримечательностью: рестораны, кафе, пабы, бары.', callback_data='city8')
            keyboard.add(key_city8)
            key_city9 = types.InlineKeyboardButton(text='Достопримечательности для детей: аквапарки, детские городки, цирк и тому подобное - то же условно, потому, как аквапарки, зоопарки и цирк интересны не только детям, но и взрослым.', callback_data='city9')
            keyboard.add(key_city9)
            bot.send_message(call.message.chat.id, 'Выберите нужную для вас достопримечательность:', reply_markup=keyboard)
        if call.data == 'city10':
            keyboard = types.InlineKeyboardMarkup()  # наша клавиатура
            key_city1 = types.InlineKeyboardButton(text='Военно-патриотические - это все объекты с военными действиями.', callback_data='city1')  # кнопка «Да»
            keyboard.add(key_city1)  # добавляем кнопку в клавиатуру
            key_city2 = types.InlineKeyboardButton(text='Культурные объекты - театры, концертные залы, кинотеатры - всё, что связано с искусством.', callback_data='city2')
            keyboard.add(key_city2)
            key_city3 = types.InlineKeyboardButton(text='Развлекательные объекты - казино, боулинг, караоке', callback_data='city3')
            keyboard.add(key_city3)
            key_city4 = types.InlineKeyboardButton(text='Религиозные объекты - церкви, костелы, кирхи, синагоги, капища, языческие идолы и валуны', callback_data='city4')
            keyboard.add(key_city4)
            key_city5 = types.InlineKeyboardButton(text='Исторические объекты - для это все достопримечательности, которые старше ста лет.', callback_data='city5')
            keyboard.add(key_city5)
            key_city6 = types.InlineKeyboardButton(text='Архитектурные объекты - здания, скульптурные композиции, фонтаны.', callback_data='city6')
            keyboard.add(key_city6)
            key_city7 = types.InlineKeyboardButton(text='Природные объекты - национальные парки, заповедники, зоопарки, гейзеры, водоемы - сюда же относится пляжный отдых и рыбалка.', callback_data='city7')
            keyboard.add(key_city7)
            key_city8 = types.InlineKeyboardButton(text='Общепит - так же может быть достопримечательностью: рестораны, кафе, пабы, бары.', callback_data='city8')
            keyboard.add(key_city8)
            key_city9 = types.InlineKeyboardButton(text='Достопримечательности для детей: аквапарки, детские городки, цирк и тому подобное - то же условно, потому, как аквапарки, зоопарки и цирк интересны не только детям, но и взрослым.', callback_data='city9')
            keyboard.add(key_city9)
            bot.send_message(call.message.chat.id, 'Выберите нужную для вас достопримечательность:', reply_markup=keyboard)
        if call.data == 'city11':
            keyboard = types.InlineKeyboardMarkup()  # наша клавиатура
            key_city1 = types.InlineKeyboardButton(text='Военно-патриотические - это все объекты с военными действиями.', callback_data='city1')  # кнопка «Да»
            keyboard.add(key_city1)  # добавляем кнопку в клавиатуру
            key_city2 = types.InlineKeyboardButton(text='Культурные объекты - театры, концертные залы, кинотеатры - всё, что связано с искусством.', callback_data='city2')
            keyboard.add(key_city2)
            key_city3 = types.InlineKeyboardButton(text='Развлекательные объекты - казино, боулинг, караоке', callback_data='city3')
            keyboard.add(key_city3)
            key_city4 = types.InlineKeyboardButton(text='Религиозные объекты - церкви, костелы, кирхи, синагоги, капища, языческие идолы и валуны', callback_data='city4')
            keyboard.add(key_city4)
            key_city5 = types.InlineKeyboardButton(text='Исторические объекты - для это все достопримечательности, которые старше ста лет.', callback_data='city5')
            keyboard.add(key_city5)
            key_city6 = types.InlineKeyboardButton(text='Архитектурные объекты - здания, скульптурные композиции, фонтаны.', callback_data='city6')
            keyboard.add(key_city6)
            key_city7 = types.InlineKeyboardButton(text='Природные объекты - национальные парки, заповедники, зоопарки, гейзеры, водоемы - сюда же относится пляжный отдых и рыбалка.', callback_data='city7')
            keyboard.add(key_city7)
            key_city8 = types.InlineKeyboardButton(text='Общепит - так же может быть достопримечательностью: рестораны, кафе, пабы, бары.', callback_data='city8')
            keyboard.add(key_city8)
            key_city9 = types.InlineKeyboardButton(text='Достопримечательности для детей: аквапарки, детские городки, цирк и тому подобное - то же условно, потому, как аквапарки, зоопарки и цирк интересны не только детям, но и взрослым.',callback_data='city9')
            keyboard.add(key_city9)
            bot.send_message(call.message.chat.id, 'Выберите нужную для вас достопримечательность:', reply_markup=keyboard)
        if call.data == 'city12':
            keyboard = types.InlineKeyboardMarkup()  # наша клавиатура
            key_city1 = types.InlineKeyboardButton(text='Военно-патриотические - это все объекты с военными действиями.', callback_data='city1')  # кнопка «Да»
            keyboard.add(key_city1)  # добавляем кнопку в клавиатуру
            key_city2 = types.InlineKeyboardButton(text='Культурные объекты - театры, концертные залы, кинотеатры - всё, что связано с искусством.', callback_data='city2')
            keyboard.add(key_city2)
            key_city3 = types.InlineKeyboardButton(text='Развлекательные объекты - казино, боулинг, караоке', callback_data='city3')
            keyboard.add(key_city3)
            key_city4 = types.InlineKeyboardButton(text='Религиозные объекты - церкви, костелы, кирхи, синагоги, капища, языческие идолы и валуны', callback_data='city4')
            keyboard.add(key_city4)
            key_city5 = types.InlineKeyboardButton(text='Исторические объекты - для это все достопримечательности, которые старше ста лет.', callback_data='city5')
            keyboard.add(key_city5)
            key_city6 = types.InlineKeyboardButton(text='Архитектурные объекты - здания, скульптурные композиции, фонтаны.', callback_data='city6')
            keyboard.add(key_city6)
            key_city7 = types.InlineKeyboardButton(text='Природные объекты - национальные парки, заповедники, зоопарки, гейзеры, водоемы - сюда же относится пляжный отдых и рыбалка.', callback_data='city7')
            keyboard.add(key_city7)
            key_city8 = types.InlineKeyboardButton(text='Общепит - так же может быть достопримечательностью: рестораны, кафе, пабы, бары.', callback_data='city8')
            keyboard.add(key_city8)
            key_city9 = types.InlineKeyboardButton(text='Достопримечательности для детей: аквапарки, детские городки, цирк и тому подобное - то же условно, потому, как аквапарки, зоопарки и цирк интересны не только детям, но и взрослым.', callback_data='city9')
            keyboard.add(key_city9)
            bot.send_message(call.message.chat.id, 'Выберите нужную для вас достопримечательность:', reply_markup=keyboard)
        if call.data == 'city13':
            keyboard = types.InlineKeyboardMarkup()  # наша клавиатура
            key_city1 = types.InlineKeyboardButton(text='Военно-патриотические - это все объекты с военными действиями.', callback_data='city1')  # кнопка «Да»
            keyboard.add(key_city1)  # добавляем кнопку в клавиатуру
            key_city2 = types.InlineKeyboardButton(text='Культурные объекты - театры, концертные залы, кинотеатры - всё, что связано с искусством.', callback_data='city2')
            keyboard.add(key_city2)
            key_city3 = types.InlineKeyboardButton(text='Развлекательные объекты - казино, боулинг, караоке', callback_data='city3')
            keyboard.add(key_city3)
            key_city4 = types.InlineKeyboardButton(text='Религиозные объекты - церкви, костелы, кирхи, синагоги, капища, языческие идолы и валуны', callback_data='city4')
            keyboard.add(key_city4)
            key_city5 = types.InlineKeyboardButton(text='Исторические объекты - для это все достопримечательности, которые старше ста лет.', callback_data='city5')
            keyboard.add(key_city5)
            key_city6 = types.InlineKeyboardButton(text='Архитектурные объекты - здания, скульптурные композиции, фонтаны.', callback_data='city6')
            keyboard.add(key_city6)
            key_city7 = types.InlineKeyboardButton(text='Природные объекты - национальные парки, заповедники, зоопарки, гейзеры, водоемы - сюда же относится пляжный отдых и рыбалка.', callback_data='city7')
            keyboard.add(key_city7)
            key_city8 = types.InlineKeyboardButton(text='Общепит - так же может быть достопримечательностью: рестораны, кафе, пабы, бары.', callback_data='city8')
            keyboard.add(key_city8)
            key_city9 = types.InlineKeyboardButton(text='Достопримечательности для детей: аквапарки, детские городки, цирк и тому подобное - то же условно, потому, как аквапарки, зоопарки и цирк интересны не только детям, но и взрослым.', callback_data='city9')
            keyboard.add(key_city9)
            bot.send_message(call.message.chat.id, 'Выберите нужную для вас достопримечательность:',reply_markup=keyboard)
        if call.data == 'city14':
            keyboard = types.InlineKeyboardMarkup()  # наша клавиатура
            key_city1 = types.InlineKeyboardButton(text='Военно-патриотические - это все объекты связанные с военными действиями.', callback_data='city1')  # кнопка «Да»
            keyboard.add(key_city1)  # добавляем кнопку в клавиатуру
            key_city2 = types.InlineKeyboardButton(text='Культурные объекты - театры, концертные залы, кинотеатры - всё, что связано с искусством.', callback_data='city2')
            keyboard.add(key_city2)
            key_city3 = types.InlineKeyboardButton(text='Развлекательные объекты - казино, боулинг, караоке', callback_data='city3')
            keyboard.add(key_city3)
            key_city4 = types.InlineKeyboardButton(text='Религиозные объекты - церкви, костелы, кирхи, синагоги, капища, языческие идолы и валуны', callback_data='city4')
            keyboard.add(key_city4)
            key_city5 = types.InlineKeyboardButton(text='Исторические объекты - для это все достопримечательности, которые старше ста лет.', callback_data='city5')
            keyboard.add(key_city5)
            key_city6 = types.InlineKeyboardButton(text='Архитектурные объекты - здания, скульптурные композиции, фонтаны.', callback_data='city6')
            keyboard.add(key_city6)
            key_city7 = types.InlineKeyboardButton(text='Природные объекты - национальные парки, заповедники, зоопарки, гейзеры, водоемы - сюда же относится пляжный отдых и рыбалка.', callback_data='city7')
            keyboard.add(key_city7)
            key_city8 = types.InlineKeyboardButton(text='Общепит - так же может быть достопримечательностью: рестораны, кафе, пабы, бары.', callback_data='city8')
            keyboard.add(key_city8)
            key_city9 = types.InlineKeyboardButton(text='Достопримечательности для детей: аквапарки, детские городки, цирк и тому подобное - то же условно, потому, как аквапарки, зоопарки и цирк интересны не только детям, но и взрослым.', callback_data='city9')
            keyboard.add(key_city9)
            bot.send_message(call.message.chat.id, 'Выберите нужную для вас достопримечательность:',reply_markup=keyboard)
        if call.data == 'city15':
            keyboard = types.InlineKeyboardMarkup()  # наша клавиатура
            key_city1 = types.InlineKeyboardButton(text='Военно-патриотические - это все объекты с военными действиями.', callback_data='city1')  # кнопка «Да»
            keyboard.add(key_city1)  # добавляем кнопку в клавиатуру
            key_city2 = types.InlineKeyboardButton(text='Культурные объекты - театры, концертные залы, кинотеатры - всё, что связано с искусством.', callback_data='city2')
            keyboard.add(key_city2)
            key_city3 = types.InlineKeyboardButton(text='Развлекательные объекты - казино, боулинг, караоке', callback_data='city3')
            keyboard.add(key_city3)
            key_city4 = types.InlineKeyboardButton(text='Религиозные объекты - церкви, костелы, кирхи, синагоги, капища, языческие идолы и валуны', callback_data='city4')
            keyboard.add(key_city4)
            key_city5 = types.InlineKeyboardButton(text='Исторические объекты - для это все достопримечательности, которые старше ста лет.', callback_data='city5')
            keyboard.add(key_city5)
            key_city6 = types.InlineKeyboardButton(text='Архитектурные объекты - здания, скульптурные композиции, фонтаны.', callback_data='city6')
            keyboard.add(key_city6)
            key_city7 = types.InlineKeyboardButton(text='Природные объекты - национальные парки, заповедники, зоопарки, гейзеры, водоемы - сюда же относится пляжный отдых и рыбалка.', callback_data='city7')
            keyboard.add(key_city7)
            key_city8 = types.InlineKeyboardButton(text='Общепит - так же может быть достопримечательностью: рестораны, кафе, пабы, бары.', callback_data='city8')
            keyboard.add(key_city8)
            key_city9 = types.InlineKeyboardButton(text='Достопримечательности для детей: аквапарки, детские городки, цирк и тому подобное - то же условно, потому, как аквапарки, зоопарки и цирк интересны не только детям, но и взрослым.', callback_data='city9')
            keyboard.add(key_city9)
            bot.send_message(call.message.chat.id, 'Выберите нужную для вас достопримечательность:',reply_markup=keyboard)
        if call.data == 'city16':
            keyboard = types.InlineKeyboardMarkup()  # наша клавиатура
            key_city1 = types.InlineKeyboardButton(text='Военно-патриотические - это все объекты с военными действиями.', callback_data='city1')  # кнопка «Да»
            keyboard.add(key_city1)  # добавляем кнопку в клавиатуру
            key_city2 = types.InlineKeyboardButton(text='Культурные объекты - театры, концертные залы, кинотеатры - всё, что связано с искусством.', callback_data='city2')
            keyboard.add(key_city2)
            key_city3 = types.InlineKeyboardButton(text='Развлекательные объекты - казино, боулинг, караоке', callback_data='city3')
            keyboard.add(key_city3)
            key_city4 = types.InlineKeyboardButton(text='Религиозные объекты - церкви, костелы, кирхи, синагоги, капища, языческие идолы и валуны', callback_data='city4')
            keyboard.add(key_city4)
            key_city5 = types.InlineKeyboardButton(text='Исторические объекты - для это все достопримечательности, которые старше ста лет.', callback_data='city5')
            keyboard.add(key_city5)
            key_city6 = types.InlineKeyboardButton(text='Архитектурные объекты - здания, скульптурные композиции, фонтаны.', callback_data='city6')
            keyboard.add(key_city6)
            key_city7 = types.InlineKeyboardButton(text='Природные объекты - национальные парки, заповедники, зоопарки, гейзеры, водоемы - сюда же относится пляжный отдых и рыбалка.', callback_data='city7')
            keyboard.add(key_city7)
            key_city8 = types.InlineKeyboardButton(text='Общепит - так же может быть достопримечательностью: рестораны, кафе, пабы, бары.', callback_data='city8')
            keyboard.add(key_city8)
            key_city9 = types.InlineKeyboardButton(text='Достопримечательности для детей: аквапарки, детские городки, цирк и тому подобное - то же условно, потому, как аквапарки, зоопарки и цирк интересны не только детям, но и взрослым.', callback_data='city9')
            keyboard.add(key_city9)
            bot.send_message(call.message.chat.id, 'Выберите нужную для вас достопримечательность:',reply_markup=keyboard)
        if call.data == 'city17':
            keyboard = types.InlineKeyboardMarkup()  # наша клавиатура
            key_city1 = types.InlineKeyboardButton(text='Военно-патриотические - это все объекты с военными действиями.', callback_data='city1')  # кнопка «Да»
            keyboard.add(key_city1)  # добавляем кнопку в клавиатуру
            key_city2 = types.InlineKeyboardButton(text='Культурные объекты - театры, концертные залы, кинотеатры - всё, что связано с искусством.', callback_data='city2')
            keyboard.add(key_city2)
            key_city3 = types.InlineKeyboardButton(text='Развлекательные объекты - казино, боулинг, караоке', callback_data='city3')
            keyboard.add(key_city3)
            key_city4 = types.InlineKeyboardButton(text='Религиозные объекты - церкви, костелы, кирхи, синагоги, капища, языческие идолы и валуны', callback_data='city4')
            keyboard.add(key_city4)
            key_city5 = types.InlineKeyboardButton(text='Исторические объекты - для это все достопримечательности, которые старше ста лет.', callback_data='city5')
            keyboard.add(key_city5)
            key_city6 = types.InlineKeyboardButton(text='Архитектурные объекты - здания, скульптурные композиции, фонтаны.', callback_data='city6')
            keyboard.add(key_city6)
            key_city7 = types.InlineKeyboardButton(text='Природные объекты - национальные парки, заповедники, зоопарки, гейзеры, водоемы - сюда же относится пляжный отдых и рыбалка.', callback_data='city7')
            keyboard.add(key_city7)
            key_city8 = types.InlineKeyboardButton(text='Общепит - так же может быть достопримечательностью: рестораны, кафе, пабы, бары.', callback_data='city8')
            keyboard.add(key_city8)
            key_city9 = types.InlineKeyboardButton(text='Достопримечательности для детей: аквапарки, детские городки, цирк и тому подобное - то же условно, потому, как аквапарки, зоопарки и цирк интересны не только детям, но и взрослым.', callback_data='city9')
            keyboard.add(key_city9)
            bot.send_message(call.message.chat.id, 'Выберите нужную для вас достопримечательность:',reply_markup=keyboard)
        if call.data == 'city18':
            keyboard = types.InlineKeyboardMarkup()  # наша клавиатура
            key_city1 = types.InlineKeyboardButton(text='Военно-патриотические - это все объекты с военными действиями.', callback_data='city1')  # кнопка «Да»
            keyboard.add(key_city1)  # добавляем кнопку в клавиатуру
            key_city2 = types.InlineKeyboardButton(text='Культурные объекты - театры, концертные залы, кинотеатры - всё, что связано с искусством.', callback_data='city2')
            keyboard.add(key_city2)
            key_city3 = types.InlineKeyboardButton(text='Развлекательные объекты - казино, боулинг, караоке', callback_data='city3')
            keyboard.add(key_city3)
            key_city4 = types.InlineKeyboardButton(text='Религиозные объекты - церкви, костелы, кирхи, синагоги, капища, языческие идолы и валуны', callback_data='city4')
            keyboard.add(key_city4)
            key_city5 = types.InlineKeyboardButton(text='Исторические объекты - для это все достопримечательности, которые старше ста лет.', callback_data='city5')
            keyboard.add(key_city5)
            key_city6 = types.InlineKeyboardButton(text='Архитектурные объекты - здания, скульптурные композиции, фонтаны.', callback_data='city6')
            keyboard.add(key_city6)
            key_city7 = types.InlineKeyboardButton(text='Природные объекты - национальные парки, заповедники, зоопарки, гейзеры, водоемы - сюда же относится пляжный отдых и рыбалка.', callback_data='city7')
            keyboard.add(key_city7)
            key_city8 = types.InlineKeyboardButton(text='Общепит - так же может быть достопримечательностью: рестораны, кафе, пабы, бары.', callback_data='city8')
            keyboard.add(key_city8)
            key_city9 = types.InlineKeyboardButton(text='Достопримечательности для детей: аквапарки, детские городки, цирк и тому подобное - то же условно, потому, как аквапарки, зоопарки и цирк интересны не только детям, но и взрослым.', callback_data='city9')
            keyboard.add(key_city9)
            bot.send_message(call.message.chat.id, 'Выберите нужную для вас достопримечательность:',reply_markup=keyboard)
        if call.data == 'city19':
            keyboard = types.InlineKeyboardMarkup()  # наша клавиатура
            key_city1 = types.InlineKeyboardButton(text='Военно-патриотические - это все объекты с военными действиями.', callback_data='city1')  # кнопка «Да»
            keyboard.add(key_city1)  # добавляем кнопку в клавиатуру
            key_city2 = types.InlineKeyboardButton(text='Культурные объекты - театры, концертные залы, кинотеатры - всё, что связано с искусством.', callback_data='city2')
            keyboard.add(key_city2)
            key_city3 = types.InlineKeyboardButton(text='Развлекательные объекты - казино, боулинг, караоке', callback_data='city3')
            keyboard.add(key_city3)
            key_city4 = types.InlineKeyboardButton(text='Религиозные объекты - церкви, костелы, кирхи, синагоги, капища, языческие идолы и валуны', callback_data='city4')
            keyboard.add(key_city4)
            key_city5 = types.InlineKeyboardButton(text='Исторические объекты - для это все достопримечательности, которые старше ста лет.', callback_data='city5')
            keyboard.add(key_city5)
            key_city6 = types.InlineKeyboardButton(text='Архитектурные объекты - здания, скульптурные композиции, фонтаны.', callback_data='city6')
            keyboard.add(key_city6)
            key_city7 = types.InlineKeyboardButton(text='Природные объекты - национальные парки, заповедники, зоопарки, гейзеры, водоемы - сюда же относится пляжный отдых и рыбалка.', callback_data='city7')
            keyboard.add(key_city7)
            key_city8 = types.InlineKeyboardButton(text='Общепит - так же может быть достопримечательностью: рестораны, кафе, пабы, бары.', callback_data='city8')
            keyboard.add(key_city8)
            key_city9 = types.InlineKeyboardButton(text='Достопримечательности для детей: аквапарки, детские городки, цирк и тому подобное - то же условно, потому, как аквапарки, зоопарки и цирк интересны не только детям, но и взрослым.', callback_data='city9')
            keyboard.add(key_city9)
            bot.send_message(call.message.chat.id, 'Выберите нужную для вас достопримечательность:',reply_markup=keyboard)
# Запускаем бота
bot.polling(none_stop=True, interval=0)
