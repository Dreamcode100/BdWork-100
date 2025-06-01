<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Pro Account Settings</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-100 min-h-screen flex items-center justify-center p-4">
  <div class="bg-white shadow-lg rounded-lg p-6 w-full max-w-3xl">
    <h2 class="text-2xl font-bold text-blue-700 mb-6 text-center">Pro Account Settings</h2>
    <form class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4">
      <div class="flex flex-col">
        <label class="text-gray-700 mb-1" for="proActivationCost">Activation Cost (৳)</label>
        <input id="proActivationCost" type="number" min="0" step="0.01" class="w-full border rounded px-3 py-2 focus:outline-none focus:ring-2 focus:ring-blue-400" />
      </div>
      <div class="flex flex-col">
        <label class="text-gray-700 mb-1" for="proDailyBonus">Daily Bonus (৳)</label>
        <input id="proDailyBonus" type="number" min="0" step="0.01" class="w-full border rounded px-3 py-2 focus:outline-none focus:ring-2 focus:ring-blue-400" />
      </div>
      <div class="flex flex-col">
        <label class="text-gray-700 mb-1" for="proValidity">Validity (days)</label>
        <input id="proValidity" type="number" min="1" step="1" class="w-full border rounded px-3 py-2 focus:outline-none focus:ring-2 focus:ring-blue-400" />
      </div>
    </form>
    <div class="mt-6 flex justify-end">
      <button id="updateProSettings" class="bg-blue-600 hover:bg-blue-700 text-white font-medium px-6 py-2 rounded transition duration-200">Update</button>
    </div>
  </div>

  <!-- Firebase Scripts -->
  <script type="module">
    import { initializeApp } from "https://www.gstatic.com/firebasejs/10.12.0/firebase-app.js";
    import {
      getFirestore,
      doc,
      getDoc,
      setDoc
    } from "https://www.gstatic.com/firebasejs/10.12.0/firebase-firestore.js";
    import {
      getAuth,
      onAuthStateChanged,
      signOut
    } from "https://www.gstatic.com/firebasejs/10.12.0/firebase-auth.js";

    const firebaseConfig = {
      apiKey: "AIzaSyCkYWvYNsg2-CR88Js6gcP2nXfvwI4TW30",
      authDomain: "bdwork-346d3.firebaseapp.com",
      projectId: "bdwork-346d3",
      storageBucket: "bdwork-346d3.appspot.com",
      messagingSenderId: "900963179093",
      appId: "1:900963179093:web:81e42d67bb31d603cc92dc",
      measurementId: "G-FM1YJ8E5GK"
    };

    const app = initializeApp(firebaseConfig);
    const db = getFirestore(app);
    const auth = getAuth(app);

    const proActivationCostInput = document.getElementById("proActivationCost");
    const proDailyBonusInput = document.getElementById("proDailyBonus");
    const proValidityInput = document.getElementById("proValidity");
    const updateProSettingsBtn = document.getElementById("updateProSettings");

    const proSettingsDocRef = doc(db, "settings", "proAccount");

    onAuthStateChanged(auth, (user) => {
      if (!user) {
        window.location.href = "login.html";
      } else {
        loadProSettings();
      }
    });

    async function loadProSettings() {
      try {
        const docSnap = await getDoc(proSettingsDocRef);
        if (docSnap.exists()) {
          const data = docSnap.data();
          proActivationCostInput.value = data.activationCost ?? "";
          proDailyBonusInput.value = data.dailyBonus ?? "";
          proValidityInput.value = data.validity ?? "";
        }
      } catch (error) {
        console.error("Error loading Pro Account Settings:", error);
      }
    }

    updateProSettingsBtn.addEventListener("click", async () => {
      const activationCost = parseFloat(proActivationCostInput.value);
      const dailyBonus = parseFloat(proDailyBonusInput.value);
      const validity = parseInt(proValidityInput.value);

      if (
        isNaN(activationCost) || activationCost < 0 ||
        isNaN(dailyBonus) || dailyBonus < 0 ||
        isNaN(validity) || validity < 1
      ) {
        alert("Please enter valid values for all fields.");
        return;
      }

      try {
        await setDoc(proSettingsDocRef, {
          activationCost,
          dailyBonus,
          validity
        });
        alert("Pro Account Settings updated successfully!");
      } catch (error) {
        alert("Failed to update settings.");
        console.error(error);
      }
    });
  </script>
</body>
</html>
