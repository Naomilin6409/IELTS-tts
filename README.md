<html>
  <body>
    <script>
      function speak(text){
        const msg = new SpeechSynthesisUtterance(text);
        window.speechSynthesis.speak(msg);
      }

      // ✅ This listens for messages from Thunkable
      document.addEventListener("message", function(e) {
        speak(e.data);
      });
    </script>
  </body>
</html>
