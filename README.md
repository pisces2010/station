# Part1
student_record = {
    'id1':{'name': 'Sara' , 'class':'V' , 'subject': 'english, math, science'},
    'id2':{'name': 'Ali' ,'class': 'V' , 'subject': 'english, math, science'},
    'id3':{'name': 'Sara' , 'class':'V' , 'subject': 'english, math, science'},
    'id4':{'name':'Suraya' , 'class':'V' , 'subject': 'english, math ,coding'}
}
print("Original student record:",student_record)


# Part2
print("")
print("Detail of id1:")
print(student_record.get('id1' , 'Not Found'))

print("")
print("Detail of id5:")
print(student_record.get('id5' , 'Not Found'))


# Part3
student_record['id5'] = {'name':'Anaya' , 'class':'V' , 'subject': 'english, art, math'}

print("")
print("After adding id5:")
print(student_record)


# Part4
student_record['id2']['subject'] = 'english, math, coding'

print("")
print("After update:")
print(student_record['id2'])

# Part5
cleared_data = {}
seen_record =[]

for student_id, details in student_record.items():
    unique_key = (details['name'], details['class'], details['subject'])

    if unique_key not in seen_record:
        seen_record.append(unique_key)
        cleared_data[student_id] = details

student_record= cleared_data

print("")
print("After removing duplicate data:")
print(student_record)


# Part6
removed_student= student_record.pop('id4' , 'student not found')

print("")
print("After Removing id4")
print(student_record)


# part7
print("The number of students left:",len(student_record))


# Part8
print("")
print("======Final Record of Students======")

for student_id, details in student_record.items():
    print(student_id,':',details)

print("===========================================")
