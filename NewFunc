import argparse

student_list = []
my_string = "Турсынов Нурдаулет Мадиярулы; 20 лет Студент 3 курса; Тешебаев Ералы Муратбекулы; 20 лет Студент 3 курса; Арман Максат Бакыт; 20 лет студент 3 курса;"


# Студент косу.
def get_student(s, student_list):
    s = s.replace(';', "")
    list_of_student_temp = s.split(" ")  # студенттерді сактау

    while len(list_of_student_temp) != 0:
        about_student = []
        about_student.append(list_of_student_temp[0:3])  # ФИО
        about_student.append(int(list_of_student_temp[3:4][0]))  # Жас
        about_student.append(int(list_of_student_temp[6:7][0]))  # Курc
        student_list.append(about_student)
        list_of_student_temp = list_of_student_temp[8:]
    return student_list


# Удаление студента студенттер тізімінен.(по ФИО, возрасту и курсу)

def delete_student(student_list, name, age, course):
    for i in range(len(student_list)):
        if (" ".join(student_list[i][0]) == name and student_list[i][1] == age and course == student_list[i][2]):
            student_list.pop(i)
            return student_list
    print("Такого студента не существует!")


# Информация шыгару
def show_by_surname(student_list, surname):
    for i in range(len(student_list)):
        if (student_list[i][0][0] == surname):
            print("ФИО: ", " ".join(student_list[i][0]), "| Возраст: ", student_list[i][1], "| Курс:",
                  student_list[i][2])


if __name__ == '__main__':
    get_student(my_string, student_list)
    func_choice = input('1) Студент қосу 2) Студент өшіру 3) Шығару')
    if func_choice == '1':
        choice = input(
            'Студент косу. Введите ФИО Возраст Курс. Пример -  Бакыт Жалгас Каанат; 18 лет Студент 1 курса;')
        print(get_student(choice, student_list))
    elif func_choice == '2':
        choice = input('Удаление студента. Введите ФИО Возраст Курс. Пример - Бакыт Жалгас Каанат 18 1 курс').split()
        print(choice)
        name = choice[0] + ' ' + choice[1] + ' ' + choice[2]
        print(name)
        age = int(choice[3])
        course = int(choice[4])
        print(delete_student(student_list, name, age, course))
    elif func_choice == '3':
        choice = input('Вывод информации о студенте. Пример - Бакыт')
        show_by_surname(student_list, choice)
