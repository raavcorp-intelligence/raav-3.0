Souce File for the RAAV Architecture: 

Speech Recognition:
Javascript {
    https://www.talater.com/annyang/ (Fast)
    https://javascript.plainenglish.io/how-to-use-speech-recognition-and-speech-synthesis-in-javascript-9bcb213f6ddd (Other built in browser methods)
}
Python {
    https://pypi.org/project/SpeechRecognition/ (Slow) (Online)
    https://stackoverflow.com/questions/38808776/python-pocketsphinx-recognition-from-the-microphone (Not as acurate) (Offline)
}



Workflow:

Javascript webpage will be the main speech recognition input as of March 2021 becuase of the effencecy of the speech recognition.
The javascript will then ping a webpage that is a PHP page that is listening for the text and other things. It will send the commmand that was sent and other varibles to be designed later.
(
    In early versions we want to encorparate the pure "commands" feature for annayang becuase that will simplify the post feature.
    We will also encorparate it so that it is fully JS until we can finalize the program to send data back to the JS.
)

Once the PHP page recives the POST then it will start a python script so that it can decipher.

```
    Documentation for annaying, we will need a wake word (RAAV) and then we can use the splat feature:
    // annyang will capture anything after a splat (*) and pass it to the function.
    // e.g. saying "Show me Batman and Robin" is the same as calling showFlickr('Batman and Robin');

    That way we can acually listen for different commands.

    // By defining a part of the following command as optional, annyang will respond to both:
    // "say hello to my little friend" as well as "say hello friend"
    'say hello (to my little) friend': greeting

    This might be helpful for some variation in the way that I ask for a source.