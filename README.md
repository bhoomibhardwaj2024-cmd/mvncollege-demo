# mvncollege-demo
this is my first Git repository
<br>
author- Bhoomi
# # import speech_recognition as sr
# # import webbrowser
# # import pyttsx3
# # import musicLibrary
# # recognizer = sr.Recognizer()
# # engine = pyttsx3.init()

# # def speak(text):
# #     engine.say(text)
# #     engine.runAndWait()

# # def processCommand(c):
# #    if "open google" in c.lower():
# #      webbrowser.open("http://google.com")
# #    elif "open facebook" in c.lower():
# #       webbrowser.open("http://facebook.com")
# #    elif "open youtube" in c.lower():
# #       webbrowser.open("http://youtube.com")
# #    elif "open linkedin" in c.lower():
# #       webbrowser.open("http://linkdin.com")
# #    elif c.lower().startswith("play"):
# #       song=c.lower().split(" ")[1]
# #       link=musicLibrary.music[song]
# #       webbrowser.open(link)
# # if __name__== "__main__":
# #     speak("Initilalising Jarvis....")
# #     while True:
# #     # listen for wake word "Jarvis"
# #        # obtain audio from the microphone
# #         r=sr.Recognizer()
# #         with sr.Microphone() as source:
# #           print("Listening...")

# #           audio = r.listen(source)
    
# #        # recognize speech using google
# #         print("recognizing....")
# #         try:
# #             with sr.Microphone() as source:
# #              print("Listening...")
# #              audio=r.listen(source,timeout=2,phrase_time_limit=1)

# #              word=r.recognize_google(audio)
# #             if(word.lower()=="jarvis"):
# #                speak("Ya")
# #             #    Listen for command
# #             with sr.Microphone() as source:
# #              print("Jarvis Active....")
# #              audio=r.listen(source)

# #              command=r.recognize_google(audio)
# #             processCommand(command)
       
# #         except Exception as e:
# #          print(" Error; {0}".format(e))



         

# import speech_recognition as sr
# import webbrowser
# import pyttsx3
# import musicLibrary  # Assumes musicLibrary.music is a dictionary of song name -> YouTube URL

# recognizer = sr.Recognizer()
# engine = pyttsx3.init()

# def speak(text):
#     engine.say(text)
#     engine.runAndWait()

# def processCommand(c):
#     c = c.lower()
    
#     if "open google" in c:
#         speak("Opening Google")
#         webbrowser.open("https://www.google.com")

#     elif "open facebook" in c:
#         speak("Opening Facebook")
#         webbrowser.open("https://www.facebook.com")

#     elif "open youtube" in c:
#         speak("Opening YouTube")
#         webbrowser.open("https://www.youtube.com")

#     elif "open linkedin" in c:
#         speak("Opening LinkedIn")
#         webbrowser.open("https://www.linkedin.com")

#     elif c.startswith("play"):
#         parts = c.split(" ")
#         if len(parts) > 1:
#             song = parts[1]
#             link = musicLibrary.music.get(song)
#             if link:
#                 speak(f"Playing {song}")
#                 webbrowser.open(link)
#             else:
#                 speak("Sorry, I couldn't find that song.")
#         else:
#             speak("Please specify a song name.")

#     else:
#         speak("Sorry, I didn't understand that command.")
   



# # let openAI Handle the request
   


# if __name__ == "__main__":
#     speak("Initializing Jarvis...")

#     while True:
#         try:
#             with sr.Microphone() as source:
#                 print("Say 'Jarvis' to activate...")
#                 recognizer.adjust_for_ambient_noise(source)
#                 audio = recognizer.listen(source, timeout=5, phrase_time_limit=3)
#                 wake_word = recognizer.recognize_google(audio)

#             if wake_word.lower() == "jarvis":
#                 speak("Yes?")
#                 with sr.Microphone() as source:
#                     print("Listening for your command...")
#                     recognizer.adjust_for_ambient_noise(source)
#                     audio = recognizer.listen(source, timeout=5, phrase_time_limit=5)
#                     command = recognizer.recognize_google(audio)
#                     processCommand(command)

#         except sr.WaitTimeoutError:
#             print("No speech detected.")
#         except sr.UnknownValueError:
#             print("Sorry, I couldn't understand.")
#         except sr.RequestError as e:
#             print(f"Speech recognition service error: {e}")
#         except Exception as e:
#             print(f"Error: {e}")
