# infosys help guide
def max_visited_speciality(patient_medical_speciality_list,medical_speciality):
    a=''
    countP=0
    countE=0
    countO=0
    for i in patient_medical_speciality_list:
        if i=='P':
           countP+=1 
        elif i=='E':
            countE+=1
        elif i=='O':
            countO+=1
    m=max(countP,countO,countE)
    if m==countP:
       a='P'
    elif m==countE:
       a='E'
    elif m==countO:
       a='O'
    speciality=medical_speciality.get(a)
    
    
    return speciality

#provide different values in the list and test your program
patient_medical_speciality_list=[301,'P',302, 'P' ,305, 'P' ,401, 'E' ,656, 'E']
medical_speciality={"P":"Pediatrics","O":"Orthopedics","E":"ENT"}
speciality=max_visited_speciality(patient_medical_speciality_list,medical_speciality)
print(speciality)
