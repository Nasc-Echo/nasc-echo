let map;
let allPins = [];

function initMap() {
    map = new google.maps.Map(document.getElementById("map"), {
        center: { lat: -12.4634, lng: 130.8456 }, // Darwin Genesis
        zoom: 12,
        styles: [ /* Insert your 'Commercial Blackout' styles here */ ]
    });
}

function openForm(category) {
    document.getElementById('form-title').innerText = "New Entry: " + category;
    document.getElementById('entry-gateway').classList.add('hidden');
    document.getElementById('form-overlay').classList.remove('hidden');
    document.getElementById('map').classList.add('blurred');
}

function closeForm() {
    document.getElementById('form-overlay').classList.add('hidden');
    document.getElementById('entry-gateway').classList.remove('hidden');
    document.getElementById('map').classList.remove('blurred');
}

function initiatePayment() {
    // This is where you connect to Stripe or Google Pay via Google Tag
    const name = document.getElementById('user-name').value;
    if(!name) { alert("Sincerity starts with a name. Please enter yours."); return; }
    
    alert("Redirecting to Secure $1.00 Verification...");
    // Successful payment triggers the Pin Drop
    confirmPin();
}

function confirmPin() {
    // Logic to save to database and drop marker with Teaser
    alert("Echo Recorded. Your Pin is now live on the Global Registry.");
    closeForm();
}
