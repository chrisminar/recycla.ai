---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<h1>Welcome to Recycla</h1>

![Recycla](/images/app_logo.jpg){: width="512" }

<p>We have a total of <span id="video-count">loading...</span> videos available.</p>

<script>
  // Import the necessary Firebase modules
  import { initializeApp } from "https://www.gstatic.com/firebasejs/9.6.10/firebase-app.js";
  import { getFirestore, collection, getDocs } from "https://www.gstatic.com/firebasejs/9.6.10/firebase-firestore.js";

  // Your Firebase configuration
  const firebaseConfig = {
    apiKey: "AIzaSyA8vgowYGKQjUW5vwhS62sp4opEPkKu31U",
    authDomain: "recyclo-c0fd1.firebaseapp.com",
    databaseURL: "https://recyclo-c0fd1-default-rtdb.firebaseio.com",
    projectId: "recyclo-c0fd1",
    storageBucket: "recyclo-c0fd1.firebasestorage.app",
    messagingSenderId: "637548885975",
    appId: "1:637548885975:web:abe5a2c27475d6c5b3bd92",
    measurementId: "G-G0BES9G9Q7"
  };

  // Initialize Firebase
  const app = initializeApp(firebaseConfig);
  const db = getFirestore(app);

  // Fetch the total number of documents in the "videos" collection
  const videoCountElement = document.getElementById('video-count');
  const videosCollection = collection(db, 'videos');
  getDocs(videosCollection)
    .then((querySnapshot) => {
      videoCountElement.textContent = querySnapshot.size;
    })
    .catch((error) => {
      console.error("Error fetching video count:", error);
      videoCountElement.textContent = "an error occurred";
    });
</script>