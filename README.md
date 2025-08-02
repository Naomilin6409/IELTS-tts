<html>
  <body>
    <script>
      function speak(text){
        const msg = new SpeechSynthesisUtterance(text);
        window.speechSynthesis.speak(msg);
      }

      // ✅ Listener for Thunkable WebViewer on Mobile
      document.addEventListener("message", function(e) {
        speak(e.data);
      });

      // ✅ Listener for Thunkable Web Preview on Desktop
      window.addEventListener("message", function(e) {
        speak(e.data);
      });

      // ✅ Debug to confirm
      document.addEventListener("message", function(e) {
        alert("Mobile received: " + e.data);
      });
      window.addEventListener("message", function(e) {
        alert("Desktop received: " + e.data);
      });
    </script>
  </body>
</html>
