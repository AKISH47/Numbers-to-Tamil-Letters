# Numbers-to-Tamil-Letters
## Convert numbers to Tamil Letters in Python

## Code ---> Take a Look at the Conversion.py file:
    def number_to_tamil(number):
       # Tamil numerals and words
       tamil_digits = ['௦', '௧', '௨', '௩', '௪', '௫', '௬', '௭', '௮', '௯']
       tamil_units = ['', 'ஒன்று', 'இரண்டு', 'மூன்று', 'நான்கு', 'ஐந்து', 'ஆறு', 'ஏழு', 'எட்டு', 'ஒன்பது']
       tamil_tens = ['', 'பத்து', 'இருபது', 'முப்பது', 'நாப்பது', 'ஐம்பது', 'அறுபது', 'எழுபது', 'எண்பது', ' 
                    தொண்ணூறு']
       tamil_hundreds = ['', 'நூறு', 'இருநூறு', 'முன்னூறு', 'நானூறு', 'ஐநூறு', 'அறுநூறு', 'எழுநூறு', 'எண்நூறு', 
                  'தொள்ளாயிரம்']
       tamil_thousands = ['', 'ஆயிரம்', 'இரண்டாயிரம்', 'மூவாயிரம்', 'நாலாயிரம்', 'ஐந்தாயிரம்', 'ஆறாயிரம்', 
                  'ஏழாயிரம்', 'எட்டாயிரம்', 'தொள்ளாயிரம்']

       if not (0 <= number <= 9999):
             return "Only numbers between 0 and 9999 are supported."

       tamil_words = []
    
       # Extract digits
       thousands = number // 1000
       hundreds = (number % 1000) // 100
       tens = (number % 100) // 10
       units = number % 10

      # Convert each place to Tamil
       if thousands:
           tamil_words.append(tamil_thousands[thousands])
       if hundreds:
           tamil_words.append(tamil_hundreds[hundreds])
       if tens:
           tamil_words.append(tamil_tens[tens])
       if units:
           tamil_words.append(tamil_units[units])
       elif not tens and not hundreds and not thousands:
           tamil_words.append(tamil_units[0])  # For zero

   return ' '.join(tamil_words)

    # Example usage
   number = int(input("Enter a number (0-9999): "))
   tamil_text = number_to_tamil(number)
   print(f"The number {number} in Tamil is: {tamil_text}")

   Have any questions on how this works? Contact me throught github!


