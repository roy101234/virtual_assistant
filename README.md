# virtual_assistant
A Virtual Assistant named F.R.I.D.A.Y. A small demonstration of how the very first form of virtual assistant works.s. 
first we need to download few modules
import pyttsx3 # pip install pyttsx3
import datetime # pre installed module
import os # preinstalled module
import random #pre installed module
import speech_recognition as sr pip install speech_recognition
from tkinter import * # preinstalled module
from PIL import ImageTk, Image # pip install pil
import pyaudio # pip install pipwin
                  then 
                 pipwin install pyaudio
                  if it doesnot work just do pipwin refresh
                  then type # pipwin install pyaudio
                  
***** write everyhthing in terminal *****



this program will work only in python language



    p = input("enter the password")
    if p == "shivam": # take the password as anything you want
        print("WELCOME BOSS")

        import pyttsx3
        import datetime
        import os
        import random
        import speech_recognition as sr
        from tkinter import *
        from PIL import ImageTk, Image


        engine=pyttsx3.init('sapi5')
        voices=engine.getProperty("voices")
        engine.setProperty('voice',voices[1].id)
        engine.setProperty("rate" , 180)
        engine.setProperty('volume',1)

        def speak(audio):
            engine.say(audio)
            engine.runAndWait()

        def takeCommand():
            r = sr.Recognizer()
            with sr.Microphone() as source:
                speak("listening boss")
                print("LISTENING BOSS.....")
                r.pause_threshold = 2
                r.energy_threshold = 50000
                audio = r.listen(source)
                try:
                    speak("recognizing boss please wait..")
                    print("RECOGNIZING BOSS.....")
                    query = r.recognize_google(audio, language='en-in')
                    print("boss said : ", query)
                    speak(f"boss said {query}")
                except Exception as e:
                    #print(e)
                    print("boss please say that again...")
                    speak("boss please say that again")
                    return "none"
                return query

        def takeCom():
            r = sr.Recognizer()
            with sr.Microphone() as source:
                #speak("listening boss")
                print("please say hey friday to begin")
                r.pause_threshold = 2
                r.energy_threshold = 50000
                audio = r.listen(source)
                try:
                    #speak("recognizing boss please wait..")
                    #print("")
                    query = r.recognize_google(audio, language='en-in')
                    #print("boss said : ", query)
                    #speak(f"boss said {query}")
                except Exception as e:
                    #print(e)
                    #print("boss please say that again...")
                    #speak("boss please say that again")
                    return "none"
                return query

        def wishme():
            speak("hello mister Mallick")
            hour = int(datetime.datetime.now().hour)
            if (hour >= 0) and (hour < 12):
                speak("good morning boss")
                strTime = datetime.datetime.now().strftime("%H:%M:%S")
                speak("The time now is")
                speak(strTime)
                print("The time is", strTime)

                y = int(datetime.datetime.now().year)
                m = int(datetime.datetime.now().month)
                d = int(datetime.datetime.now().day)
                a = ["s", "January", "February", "March", "April", "May", "June", "July", "August", "September", "October",
                     "November", "December"]
                b = a[m]
                speak(f" boss the date is {d} {b} {y} ")
                print("The current date is", d, b, y)


            elif (hour >= 12) and (hour < 18):
                speak("good afternoon boss")
                strTime = datetime.datetime.now().strftime("%H:%M:%S")
                speak("The time now is")
                speak(strTime)
                print("The time is", strTime)

                y = int(datetime.datetime.now().year)
                m = int(datetime.datetime.now().month)
                d = int(datetime.datetime.now().day)
                a = ["s", "January", "February", "March", "April", "May", "June", "July", "August", "September", "October",
                     "November", "December"]
                b = a[m]
                speak(f" boss the date is {d} {b} {y} ")
                print("The current date is", d, b, y)


            else:
                speak("good evening boss")
                strTime = datetime.datetime.now().strftime("%H:%M:%S")
                speak("The time now is")
                speak(strTime)
                print("The time is", strTime)

                y = int(datetime.datetime.now().year)
                m = int(datetime.datetime.now().month)
                d = int(datetime.datetime.now().day)
                a = ["s", "January", "February", "March", "April", "May", "June", "July", "August", "September", "October",
                     "November", "December"]
                b = a[m]
                speak(f" boss the date is {d} {b} {y} ")
                print("The current date is", d, b, y)
            speak("i am friday")
            speak("i am online and ready")
            if d == 19:
                if b == "January":
                    speak("boss mister roy specially created me for you")
                    speak("happy birthday mister mallick")
                    speak("mister roy loves you a lot as a best friend and treat you as his bestie")




        def quiz():
            speak("alright sir lets have some fun")
            print("Alright sir lets have some fun")
            speak("ok let's begin our game")
            speak("are you ready sir")
            r = input("enter your reply sir")
            c = 0
            if r == "yes":
                speak("the first one is")
                speak("What does come down but never goes up?")
                print("What does come down but never goes up?")
                a1 = input("enter your answer")

                if a1 == "rain":
                    speak("good job sir")
                    print("Good job sir")
                    c += 1

                else:
                    speak("no sir its rain actually")
                    speak("no problem sir better luck next time")
                    print("no sir its rain actually")
                    print("no problem sir better luck next time")

                speak("then the second one is")
                speak("What is a Blue Whale’s heart the same size as?")
                print("What is a Blue Whale’s heart the same size as?")
                a1 = input("enter your answer")

                if a1 == "size of a small car":
                    speak("good job sir")
                    print("Good job sir")
                    c += 1

                else:
                    speak("no sir its of the size of a small car actually")
                    speak("no problem sir better luck next time")
                    print("no sir its of the size of a small car actually")
                    print("no problem sir better luck next time")

                speak("then the third one is")
                speak("On a normal computer keyboard with which number does * share a key?")
                print("On a normal computer keyboard with which number does * share a key?")
                a1 = input("enter your answer")
                if a1 == "8":
                    speak("good job sir")
                    print("Good job sir")
                    c += 1

                else:
                    speak("no sir its 8 actually")
                    speak("no problem sir better luck next time")
                    print("no sir its 8 actually")
                    print("no problem sir better luck next time")

                speak("then the fourth one is")
                speak("Which month has 28 days?")
                print("Which month has 28 days?")
                a1 = input("enter your answer")
                if a1 == "February":
                    speak("no sir its not the correct answer")
                    print("no sir its not the correct answer")

                elif a1 == "all months has 28 days":
                    speak("good job sir")
                    print("Good job sir")
                    c += 1

                else:
                    speak("no sir its February actually")
                    speak("no problem sir better luck next time")
                    print("no sir its February actually")
                    print("no problem sir better luck next time")

                speak("then the fifth one is")
                speak("If you drop a yellow hat in the red sea what does it became ?")
                print("If you drop a yellow hat in the red sea what does it became ?")
                a1 = input("enter your answer")
                if a1 == "it becomes wet":
                    speak("good job sir")
                    print("Good job sir")
                    c += 1

                else:
                    speak("no sir it becomes wet actually")
                    speak("no problem sir better luck next time")
                    print("no sir it becomes wet actually")
                    print("no problem sir better luck next time")
                speak(f"sir your score is {c}")
                print("sir your score is", c)

            else:
                speak("alright sir no problem what else can i do for you")






        def friday():
            a = takeCom()
            query = a.lower()
            if "friday" in query:
                speak("welcome boss")
                wishme()
                #b = takeCommand()
                while True:
                    query = takeCommand().lower()

                    if "jarvis" in query:
                        speak("i am not jarvis boss mister roy has it and its password is unbreakable")


                    elif "surprise" in query:
                        m = int(datetime.datetime.now().month)
                        d = int(datetime.datetime.now().day)
                        a = ["s", "January", "February", "March", "April", "May", "June", "July", "August", "September",
                             "October",
                             "November", "December"]
                        b = a[m]
                        if d == 19:
                            if b == "January":

                                speak("sure sir")
                                speak("hello mister mallick its 19th of january and mister roy has a surprise for you")

                                root = Tk()
                                root.title("HAPPY BIRTHDAY SHIVAM")
                                root.geometry('1280x720')

                                compText = StringVar()
                                userText = StringVar()

                                userText.set("HAPPY BIRTHDAY")

                                userFrame = LabelFrame(root, text='STARTUPS', font=("Black ops one", 15, 'bold'))
                                userFrame.pack(fill='both', expand='yes')

                                left = Message(userFrame, textvariable=userText, bg="black", fg="white")

                                left.config(font=('Century Gothic', 20, 'bold'))
                                left.pack(fill='both', expand='yes')

                                compFrame = LabelFrame(root, text='🍕🍕🍕🍔🍔🍔🍰🍰🍰🍰🍰🎂🎂🎂🎂',
                                                       font=("Black ops one", 15, 'bold'))
                                compFrame.pack(fill='both', expand='yes')

                                compText.set("BRO PARTY KAAAB DEGA YAR YAAAR HAPPY BIRTHDAY FROM ME 🍕🍕🍕🍔🍔🍔🍰🍰🍰🍰🍰🎂🎂🎂🎂")

                                left1 = Message(compFrame, textvariable=compText, bg="black", fg="white")

                                left1.config(font=('Century Gothic', 20, 'bold'))
                                left1.pack(fill='both', expand='yes')

                                # bt=Button(root,text="run jarvis",font=("Black ops one", 15 ,'bold'),bg="silver",fg="indigo",command=root)
                                # bt.pack(fill="x",expand="no")

                                bt = Button(root, text="CLOSE PARTY", font=("Black ops one", 15, 'bold'), bg="silver", fg="black",
                                            command=root.destroy)
                                bt.pack(fill="x", expand="no")

                                root.mainloop()

                                music_dir = "C:\\n1"
                                songs = os.listdir(music_dir)
                                rn = random.choice(songs)
                                os.startfile(os.path.join(music_dir, rn))

                            else:
                                speak("")
                        else:
                            speak("sir today is not your birthday")



                    elif "exit" in query:
                        speak("bye sir hope you enjoyed using me")
                        break


                    elif "play quiz" in query:
                        quiz()
                        speak("sir do you want to play again")
                        an = input("enter your reply")
                        if an == "yes":
                            speak("ok sure sir at your service")
                            quiz()



                    elif "sleep" in query:
                        speak("sure sir when ever you need me call me")
                        if __name__ == "__main__":
                            friday()

            else:
                speak('you are not authorised user')
                exit()

        if __name__ == "__main__":
            friday()

    else:
        print("SORRY YOU ARE NOT AUTHORISED USER")






