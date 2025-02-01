# HomeWork16
class Student:
    def __init__(self, first_name, last_name, personal_id, birth_year, grades):
        self.first_name = first_name
        self.last_name = last_name
        self.personal_id = personal_id
        self.birth_year = birth_year
        self.grades = grades

    def __str__(self):
        grades_str = ', '.join([f"{subject}: {grade}" for subject, grade in self.grades.items()])
        return f"Student {self.first_name} {self.last_name}, Personal ID: {self.personal_id}, Birth Year: {self.birth_year}, Grades: {grades_str}"

    def years_until_18(self):
        current_year = 2025
        age = current_year - self.birth_year
        if age >= 18:
            return 0  
        return 18 - age

student1 = Student("Giorgi", "Kakabadze", "123456789", 2007, {"Math": 95, "Programming": 100})
student2 = Student("Nino", "Tsereteli", "987654321", 2006, {"Math": 88, "Programming": 92})
student3 = Student("Levan", "Jorjoliani", "567890123", 2008, {"Math": 76, "Programming": 84})
print(student1)
print(f"Years until 18 for {student1.first_name}: {student1.years_until_18()} years")

print(student2)
print(f"Years until 18 for {student2.first_name}: {student2.years_until_18()} years")

print(student3)
print(f"Years until 18 for {student3.first_name}: {student3.years_until_18()} years")
