# Password-Generator-
Да я знаю, что подобных проектов очень много, но чем примечателен этот... это тем что его создал ChatGPT/Принцип работы такой запускаешь файл через терминал py или через cmd и пишешь кол-во символов в пароле. Далее в файле где хранится файл .py появился блокнот, в котором и будет ваш пароль
Код приложения (spacecode):
import random
import string

def generate_password(length):
    # Функция для генерации случайного пароля заданной длины
    letters = string.ascii_letters + string.digits + string.punctuation
    password = ''.join(random.choice(letters) for i in range(length))
    return password

if __name__ == '__main__':
    length = int(input("Введите длину пароля: "))
    password = generate_password(length)
    print("Ваш пароль: ", password)

    with open("passwords.txt", "a") as file:
        # Сохраняем пароль в файл
        file.write(password + "\n")
