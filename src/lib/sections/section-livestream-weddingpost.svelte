<script>
  const instagramUsername = "@hinata_hyuga";
  const meetingID = "123456789";
  const meetingPass = "hariBahagia";

  const openInstagram = () => {
    window.open("https://www.instagram.com/hinata_hyuga", "_blank");
  };

  const joinStreaming = () => {
    alert("Redirecting to Live Streaming...");
    // redirect logic here
  };
</script>

<div class="bg-gray-200 max-w-2xl mx-auto px-4 py-10 font-serif border-x border-black text-gray-900">
  <!-- Title -->
    <div class="border-t-4 border-black mb-0.5"></div>
    <div class="border-t-3 border-black mb-1"></div>
    <h1 class="text-center text-3xl font-bold tracking-wide">LIVE STREAM</h1>
    <div class="border-b-3 border-black mt-1"></div>
    <div class="border-b-4 border-black mt-0.5 mb-6"></div>

  <!-- Content Layout -->
  <div class="grid md:grid-cols-2 mt-8">
    <!-- Left: Text -->
    <div class="italic text-justify px-5 leading-relaxed text-gray-800">
      <p>
        This live stream is our way of extending our arms across the globe to embrace
        each of you virtually, allowing all of you to witness, participate in, and celebrate
        our joy in real-time, no matter how many miles may separate us. Whether you're
        watching from across the country, on the other side of the world, or simply unable
        to attend due to other commitments, please know that your presence through
        the live stream will be deeply felt and genuinely appreciated. Thank you for being
        part of our lives and for finding ways to celebrate with us, near or far.
      </p>
    </div>

    <!-- Right: Content -->
    <div class="flex flex-col items-center md:border-l-3 border-black md:pl-6 space-y-8 pt-15">
        <!-- Instagram -->
        <div class="flex flex-col items-center space-y-2">
            <img src="https://cdn-icons-png.flaticon.com/512/2111/2111463.png" class="w-8 h-8" alt="Instagram" />
            <div class="text-base">@hinata_hyuga</div>
            <button
            on:click={joinStreaming}
            class="bg-black text-white px-4 py-1 rounded-full text-sm shadow hover:opacity-90"
            >
            Join Live Streaming
            </button>
        </div>

        <!-- Zoom -->
        <div class="flex flex-col items-center space-y-2">
            <img src="/zoom.png" class="w-8 h-8" alt="Zoom" />
            <div class="text-center md:text-left text-sm leading-relaxed">
            <div><span class="font-medium">ID Meeting :</span> 123456789</div>
            <div><span class="font-medium">Password :</span> hariBahagia</div>
            </div>
        </div>
    </div>
  </div>
</div>
