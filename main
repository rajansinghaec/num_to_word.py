# 4:10pm to 6:00pm
# completed in 2 hrs


def read_two_digit(num):
	#this function returns the word conversion of  number < 100
	word=''
	if(num==0):
		word='zero'
	elif(num in one_to_nineteen.keys()):
		word=one_to_nineteen[num]
	else:
		if(num in twenty_to_ninety.keys()):
			word=twenty_to_ninety[num]
		else:
	 		word=twenty_to_ninety[int(num/10)*10] + ' ' + one_to_nineteen[num%10]
	
	return word

def read_three_digit(num):
	#this function returns the word conversion of three digits value
	word=''
	if(num<100):
		return read_two_digit(num)
	else:
		word=one_to_nineteen[num//100]+' '+hundred+' '
		if(num%100!=0):
			word+=read_two_digit(num%100)
	
	return word
def indian_system(num):
	#converting the given number into list of indian system
	# Ex- 123456789 into list of [12,34,56,789]

	return [num//10000000 ,(num%10000000)//100000 , (num%100000)//1000 , num%1000]

def read_indian_system(num):
	# this is the main working function 
	# this converts 9 digits number into word of indian system
	special_word=["crore","lakh","thousand",""]
	indian_list = indian_system(num)
	
	word=''
	for i in range(-4,0):
		new_num=indian_list[i]
		if(new_num!=0):
			three_digit=read_three_digit(new_num)
			word+=three_digit+' '+special_word[i]+' '
			
		
	return word		
		

	

zero='zero'

one_to_nineteen={1:'one', 2:'two', 3:'three', 4:'four', 5:'five', 6:'six', 7:'seven', 8:'eight', 9:'nine', 10:'ten', 11:'eleven', 12:'twelve', 13:'thirteen', 14:'fourteen', 15:'fifteen', 16:'sixteen', 17:'seventeen', 18:'eighteen', 19:'nineteen'}

twenty_to_ninety={20:"twenty",30:"thirty",40:"fourty",50:"fifty",60:"sixty",70:"seventy",80:"eighty",90:"ninety"}

hundred="hundred"

while(True):
	num=int(input("\nEnter number (not more than 10 digits) : "))

	word=read_indian_system(num)
	print("\n",num," : ",word)
	
	print("\nTry again\n")
  
