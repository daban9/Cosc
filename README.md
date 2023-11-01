def to_pig_latin(sentence):
  words = sentence.split()
  result = []

  def pig_latin_translate(word):
        if len(word) == 1:
         return word + "ay"
        else:
         return word[1:] + word[0] + "ay"

  for word in words:
    pig_latin_word = pig_latin_translate(word)
    result.append(pig_latin_word)

  pig_latin_sentence = "".join(result)

  return pig_latin_sentence

if __name__ =="__main__":

   sentence = input("English: ")

   pig_latin_result = to_pig_latin(sentence)

   print("Pig Latin:", pig_latin_result)
