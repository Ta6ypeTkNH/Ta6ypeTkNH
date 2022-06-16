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
