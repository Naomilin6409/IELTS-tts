<html>
  <body>
    <script>
      document.addEventListener("message", function(e) {
        alert("Received: " + e.data);
        speak(e.data);
      });
      function speak(text){
        const msg = new SpeechSynthesisUtterance(text);
        window.speechSynthesis.speak(msg);
      }
    </script>
  </body>
</html>
