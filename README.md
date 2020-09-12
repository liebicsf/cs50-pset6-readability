from cs50 import get_string  
  
text = get_string("Text: ")  
  
letters = 0  
sentences = 0  
words = 0  
  
for i in text:  
    if i.isalpha():  
        letters += 1  
    elif i == '.' or i == '!' or i == '?':  
        sentences += 1  
    elif i.isspace():  
        words += 1  
          
words += 1  
      
grade = round(0.0588 * (100 * letters // words) - 0.296 * (100 * sentences // words) - 15.8)  
if grade < 16 and grade >= 0:  
    print(f"Grade {grade}")  
elif grade >= 16:  
    print("Grade 16+")  
else:  
    print("Before Grade 1") 
