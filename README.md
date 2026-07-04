<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Taita Taveta National Polytechnic Graduation</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght=0,600;1,600&family=Poppins:wght=300;400;600&display=swap');
        body { font-family: 'Poppins', sans-serif; }
        .font-serif { font-family: 'Playfair Display', serif; }
        .bg-pattern { background-color: #0f172a; background-image: radial-gradient(#334155 1px, transparent 1px); background-size: 20px 20px; }
    </style>
</head>
<body class="bg-pattern min-h-screen flex items-center justify-center p-4 py-12">

    <div class="bg-white rounded-3xl shadow-2xl max-w-md w-full relative overflow-hidden transform transition-all hover:scale-[1.01] duration-300">
        
        <div class="absolute top-0 left-0 w-full h-32 bg-gradient-to-br from-yellow-400 via-yellow-500 to-yellow-600">
            <div class="absolute -top-10 -right-10 w-32 h-32 bg-white opacity-20 rounded-full"></div>
            <div class="absolute -bottom-8 -left-8 w-24 h-24 bg-white opacity-20 rounded-full"></div>
        </div>

        <div class="relative z-10 px-8 pb-8 pt-12 flex flex-col items-center text-center">
            
            <div class="bg-white p-4 rounded-full shadow-lg mb-4 border-4 border-yellow-50">
                <svg xmlns="http://www.w3.org/2000/svg" width="48" height="48" viewBox="0 0 24 24" fill="none" stroke="#ca8a04" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                    <path d="M22 10v6M2 10l10-5 10 5-10 5z"/><path d="M6 12v5c3 3 9 3 12 0v-5"/>
                </svg>
            </div>

            <h2 class="text-sm font-semibold tracking-widest text-gray-400 uppercase mb-2">Taita Taveta National Polytechnic</h2>
            <h1 class="text-4xl font-serif text-gray-800 mb-2">2nd Graduation</h1>
            <h2 class="text-2xl font-serif text-yellow-600 italic mb-6">Ceremony</h2>

            <div class="mb-6 relative w-full max-w-[240px]">
                <img src="23222.jpg" alt="Graduation Portrait" class="w-full aspect-[3/4] rounded-2xl object-cover border-4 border-yellow-400 shadow-md mx-auto">
            </div>

            <div class="w-16 h-1 bg-yellow-400 rounded mb-6"></div>

            <div class="text-left w-full text-gray-600 text-sm space-y-3 mb-6 bg-gray-50 p-4 rounded-xl border border-gray-100">
                <p>📅 <strong class="text-gray-800">Date:</strong> Friday, July 10, 2026</p>
                <p>⏰ <strong class="text-gray-800">Time:</strong> 08:00 AM EAT</p>
                <p>📍 <strong class="text-gray-800">Location:</strong> Main Campus, Voi</p>
                <p>🎓 <strong class="text-gray-800">Total Graduands:</strong> 1,749</p>
                <p>👔 <strong class="text-gray-800">Chief Guest:</strong> Dr. Esther Thaara Muoria (PS, TVET)</p>
            </div>

            <div class="w-full max-w-[260px] mb-8 rounded-2xl overflow-hidden shadow-lg bg-gray-100 border border-gray-200 mx-auto">
                <video controls class="w-full aspect-[9/16] object-cover">
                    <source src="cooking-video.mp4" type="video/mp4">
                    Your browser does not support the video tag.
                </video>
            </div>

            <div class="text-left w-full text-xs text-gray-500 mb-6 space-y-2">
                <p class="font-semibold text-gray-700">Important Checklist for Graduands:</p>
                <ul class="list-disc pl-4 space-y-1">
                    <li>Verify name order on the student portal.</li>
                    <li>Clear all fee arrears and graduation/convocation fees.</li>
                    <li>Collect gowns from respective HODs using payment evidence.</li>
                </ul>
            </div>

            <div class="w-full bg-gray-50 rounded-xl p-4 mb-8 text-sm text-gray-600 border border-gray-100">
                <p class="font-semibold text-gray-800 mb-1">Send your warmest wishes!</p>
                <p>Click below to send a congratulatory message directly via WhatsApp.</p>
            </div>

            <button onclick="sendWhatsApp()" class="w-full bg-[#25D366] hover:bg-[#1ebd5a] text-white font-semibold py-4 px-6 rounded-xl transition-all duration-300 transform hover:-translate-y-1 hover:shadow-lg hover:shadow-green-500/30 flex items-center justify-center gap-3">
                Send Congratulations
            </button>
        </div>
    </div>

    <script>
        window.onload = function() {
            var duration = 3 * 1000;
            var animationEnd = Date.now() + duration;
            var defaults = { startVelocity: 30, spread: 360, ticks: 60, zIndex: 0 };
            function randomInRange(min, max) { return Math.random() * (max - min) + min; }
            var interval = setInterval(function() {
                var timeLeft = animationEnd - Date.now();
                if (timeLeft <= 0) return clearInterval(interval);
                var particleCount = 50 * (timeLeft / duration);
                confetti(Object.assign({}, defaults, { particleCount, origin: { x: randomInRange(0.1, 0.3), y: Math.random() - 0.2 } }));
                confetti(Object.assign({}, defaults, { particleCount, origin: { x: randomInRange(0.7, 0.9), y: Math.random() - 0.2 } }));
            }, 250);
        };

        function sendWhatsApp() {
            const phoneNumber = "254720975663";
            const message = "Congratulations on your graduation at Taita Taveta National Polytechnic! 🎉🙏🥂"; 
            const whatsappUrl = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(message)}`;
            window.open(whatsappUrl, '_blank');
        }
    </script>
</body>
</html>
