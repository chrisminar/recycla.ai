---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

<h1>Welcome to Recycla</h1>

<div style="display: flex; align-items: center; gap: 20px; margin-top: 20px;">
  <img src="{{ '/images/app_logo.jpg' | relative_url }}" alt="Recycla Logo" style="width: 128px" />
  <table style="width: 100%; border-collapse: collapse; text-align: center; font-size: 1.2em;">
    <thead>
      <tr style="background-color: #f2f2f2;">
        <th style="border: 1px solid #ddd; padding: 10px;">Metric</th>
        <th style="border: 1px solid #ddd; padding: 10px;">Count</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td style="border: 1px solid #ddd; padding: 10px;">Recyclas Deployed</td>
        <td style="border: 1px solid #ddd; padding: 10px;" id="pis-count">loading...</td>
      </tr>
      <tr>
        <td style="border: 1px solid #ddd; padding: 10px;">Items Recycled</td>
        <td style="border: 1px solid #ddd; padding: 10px;" id="video-count">loading...</td>
      </tr>
    </tbody>
  </table>
</div>

<script type="module">
  // Import the necessary Firebase modules
  import { initializeApp } from "https://www.gstatic.com/firebasejs/9.6.10/firebase-app.js";
  import { getFirestore, doc, getDoc } from "https://www.gstatic.com/firebasejs/9.6.10/firebase-firestore.js";

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

  // Fetch the video_counts field from the hourly_counts document in the stats collection
  const videoCountElement = document.getElementById('video-count');
  const piCountElement = document.getElementById('pis-count');
  const hourlyCountsDocRef = doc(db, 'stats', 'hourly_counts');
  getDoc(hourlyCountsDocRef)
    .then((docSnapshot) => {
      if (docSnapshot.exists()) {
        const data = docSnapshot.data();
        console.log("Fetched data:", data);
        videoCountElement.textContent = data.videos_count || "0";
        piCountElement.textContent = data.pis_count || "0";
      } else {
        console.error("Document does not exist");
        videoCountElement.textContent = "no data available";
      }
    })
    .catch((error) => {
      console.error("Error fetching video count:", error);
      videoCountElement.textContent = "an error occurred";
    });
</script>