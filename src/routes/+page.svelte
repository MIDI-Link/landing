<script>
	import Logo from "$lib/components/Logo/Logo.svelte";
	import Pack from "$lib/components/Pack/Pack.svelte";
	import SectionTitle from "$lib/components/SectionTitle/SectionTitle.svelte";
  import artists from "$lib/data/artists.json";
  import packs from "$lib/data/packs.json";
</script>
<main>

  <section class="container mx-auto pt-12 pb-24">

    <div class="flex flex-col md:flex-row justify-evenly items-center py-12">

      <div class="grid grid-cols-2 gap-4 sm:gap-8 md:gap-12 text-charcoal mb-12 md:mb-0">

        <div class="flex flex-col">
          <span class="font-bold mb-2 sm:text-lg">Dig thru the MIDI <br /> NFT library</span>
          <a href="#" class="uppercase bg-gold text-center rounded-xl py-1 px-8">Find</a>
        </div>
  
        <div class="flex flex-col">
          <span class="font-bold mb-2 sm:text-lg">Connect your <br /> instrument</span>
          <a href="#" class="uppercase bg-midiBlue text-center rounded-xl py-1 px-8">Mint</a>
        </div>
  
      </div>

      <div class="w-72">

        <Pack 
          artistName="DJ Sluggacane" 
          artistImagePath="/images/sluggacane.png" 
          coverImagePath="/images/cover-1.png"
          packName="ORN 808"
          price=".025"
        />

      </div>

    </div>

  </section>

  <!-- Latest Releases -->
  <section class="bg-[#EEF5FA] pb-24">

    <SectionTitle title="Latest Releases" />

    <div class="w-full overflow-x-scroll no-scrollbar">

      <div class="flex">

        {#each Array(5) as _, i}

        <div class="flex">

          {#each packs as pack}

            <div class="w-48 mx-4">
              <Pack 
                artistName={pack.artistName} 
                artistImagePath={pack.artistImagePath}
                coverImagePath={pack.packImagePath}
                packName={pack.packName}
                price={pack.price}
                size="sm"
              />
            </div>

          {/each}

        </div>
  
        {/each}
  
      </div>

    </div>

  </section>

  <!-- Hot Producers -->
  <section class="pb-24">

    <SectionTitle title="Trending" />

    <div class="w-full overflow-x-scroll no-scrollbar px-4">

      <div class="grid grid-rows-2 grid-flow-col gap-6">

        {#each artists as artist, i}
        <div class="w-56 flex items-center">
          <span class="w-6 mr-1">{i + 1}.</span>
          <div class="mr-2">
            <img class="rounded-full h-16 w-16" src={artist.imagePath} alt={artist.name} />
          </div>
          <div class="flex flex-col text-sm">
            <span class="text-midiBlueLink">{artist.name}</span>
            <span class="text-gray-400">MIDI: {artist.midiCount}</span>
          </div>
        </div>
        {/each}

      </div>

    </div>

  </section>

  <!-- Sell NFTs -->
  <section class="bg-gray-100 py-32">

    <div class="container mx-auto px-4 flex justify-center">

      <div class="grid grid-cols-1 sm:grid-cols-3 gap-4 max-w-4xl">

        <div class="flex flex-col bg-white shadow-md rounded-lg py-4 px-6 text-center justify-between">
          <span class="text-blue-400 text-3xl text-center font-semibold uppercase mb-1">Connect</span>
          <span class="mb-3 text-charcoal">Sync your compatible <br /> synthesizer instrument</span>
          <div class="flex justify-center">
            <a class="border border-midiBlue rounded-lg text-center text-midiBlue py-1 px-10 uppercase" href="#">Link</a>
          </div>
        </div>

        <div class="flex flex-col bg-white shadow-md rounded-lg py-4 px-6 text-center justify-between">
          <span class="text-blue-400 text-3xl text-center font-semibold uppercase mb-1">Upload</span>
          <span class="mb-3 text-charcoal">Add patches, projects, & sequences</span>
          <div class="flex justify-center">
            <a class="border border-midiBlue rounded-lg text-center text-midiBlue py-1 px-10 uppercase" href="#">Mint</a>
          </div>
        </div>

        <div class="flex flex-col bg-white shadow-md rounded-lg py-4 px-6 text-center justify-between">
          <span class="text-blue-400 text-3xl text-center font-semibold uppercase mb-1">Sell</span>
          <span class="mb-3 text-charcoal">List MIDI NFTs from your catalogue</span>
          <div class="flex justify-center">
            <a class="border border-midiBlue rounded-lg text-center text-midiBlue py-1 px-10 uppercase" href="#">List</a>
          </div>
        </div>

      </div>

    </div>

  </section>

  <div class="py-32 text-center">

    <a href="https://app.midi.link" class="uppercase bg-gold text-2xl py-3 px-6 rounded-xl">Enter Market</a>

  </div>

  <footer class="bg-gray-50">
    
    <div class="container mx-auto px-4 py-12 flex justify-between items-center md:items-end flex-col md:flex-row">

      <div class="flex flex-col order-last md:order-first mt-8 md:mt-0 items-center md:items-start">

        <!-- social icons-->
        <div class="flex mb-2">
  
          <a href="#" class="w-6 flex items-align mr-2">
            <svg fill="#696969" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512"><!--! Font Awesome Pro 6.2.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M549.655 124.083c-6.281-23.65-24.787-42.276-48.284-48.597C458.781 64 288 64 288 64S117.22 64 74.629 75.486c-23.497 6.322-42.003 24.947-48.284 48.597-11.412 42.867-11.412 132.305-11.412 132.305s0 89.438 11.412 132.305c6.281 23.65 24.787 41.5 48.284 47.821C117.22 448 288 448 288 448s170.78 0 213.371-11.486c23.497-6.321 42.003-24.171 48.284-47.821 11.412-42.867 11.412-132.305 11.412-132.305s0-89.438-11.412-132.305zm-317.51 213.508V175.185l142.739 81.205-142.739 81.201z"/></svg>
          </a>

          <a href="#" class="w-6 flex items-align mr-2">
            <svg fill="#696969" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><!--! Font Awesome Pro 6.2.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M459.37 151.716c.325 4.548.325 9.097.325 13.645 0 138.72-105.583 298.558-298.558 298.558-59.452 0-114.68-17.219-161.137-47.106 8.447.974 16.568 1.299 25.34 1.299 49.055 0 94.213-16.568 130.274-44.832-46.132-.975-84.792-31.188-98.112-72.772 6.498.974 12.995 1.624 19.818 1.624 9.421 0 18.843-1.3 27.614-3.573-48.081-9.747-84.143-51.98-84.143-102.985v-1.299c13.969 7.797 30.214 12.67 47.431 13.319-28.264-18.843-46.781-51.005-46.781-87.391 0-19.492 5.197-37.36 14.294-52.954 51.655 63.675 129.3 105.258 216.365 109.807-1.624-7.797-2.599-15.918-2.599-24.04 0-57.828 46.782-104.934 104.934-104.934 30.213 0 57.502 12.67 76.67 33.137 23.715-4.548 46.456-13.32 66.599-25.34-7.798 24.366-24.366 44.833-46.132 57.827 21.117-2.273 41.584-8.122 60.426-16.243-14.292 20.791-32.161 39.308-52.628 54.253z"/></svg>
          </a>

          <a href="#" class="w-6 flex items-align mr-2">
            <svg fill="#696969" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><!--! Font Awesome Pro 6.2.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M224.1 141c-63.6 0-114.9 51.3-114.9 114.9s51.3 114.9 114.9 114.9S339 319.5 339 255.9 287.7 141 224.1 141zm0 189.6c-41.1 0-74.7-33.5-74.7-74.7s33.5-74.7 74.7-74.7 74.7 33.5 74.7 74.7-33.6 74.7-74.7 74.7zm146.4-194.3c0 14.9-12 26.8-26.8 26.8-14.9 0-26.8-12-26.8-26.8s12-26.8 26.8-26.8 26.8 12 26.8 26.8zm76.1 27.2c-1.7-35.9-9.9-67.7-36.2-93.9-26.2-26.2-58-34.4-93.9-36.2-37-2.1-147.9-2.1-184.9 0-35.8 1.7-67.6 9.9-93.9 36.1s-34.4 58-36.2 93.9c-2.1 37-2.1 147.9 0 184.9 1.7 35.9 9.9 67.7 36.2 93.9s58 34.4 93.9 36.2c37 2.1 147.9 2.1 184.9 0 35.9-1.7 67.7-9.9 93.9-36.2 26.2-26.2 34.4-58 36.2-93.9 2.1-37 2.1-147.8 0-184.8zM398.8 388c-7.8 19.6-22.9 34.7-42.6 42.6-29.5 11.7-99.5 9-132.1 9s-102.7 2.6-132.1-9c-19.6-7.8-34.7-22.9-42.6-42.6-11.7-29.5-9-99.5-9-132.1s-2.6-102.7 9-132.1c7.8-19.6 22.9-34.7 42.6-42.6 29.5-11.7 99.5-9 132.1-9s102.7-2.6 132.1 9c19.6 7.8 34.7 22.9 42.6 42.6 11.7 29.5 9 99.5 9 132.1s2.7 102.7-9 132.1z"/></svg>
          </a>

          <a href="#" class="w-6 flex items-align mr-2">
            <svg fill="#696969" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 512"><!--! Font Awesome Pro 6.2.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M524.531,69.836a1.5,1.5,0,0,0-.764-.7A485.065,485.065,0,0,0,404.081,32.03a1.816,1.816,0,0,0-1.923.91,337.461,337.461,0,0,0-14.9,30.6,447.848,447.848,0,0,0-134.426,0,309.541,309.541,0,0,0-15.135-30.6,1.89,1.89,0,0,0-1.924-.91A483.689,483.689,0,0,0,116.085,69.137a1.712,1.712,0,0,0-.788.676C39.068,183.651,18.186,294.69,28.43,404.354a2.016,2.016,0,0,0,.765,1.375A487.666,487.666,0,0,0,176.02,479.918a1.9,1.9,0,0,0,2.063-.676A348.2,348.2,0,0,0,208.12,430.4a1.86,1.86,0,0,0-1.019-2.588,321.173,321.173,0,0,1-45.868-21.853,1.885,1.885,0,0,1-.185-3.126c3.082-2.309,6.166-4.711,9.109-7.137a1.819,1.819,0,0,1,1.9-.256c96.229,43.917,200.41,43.917,295.5,0a1.812,1.812,0,0,1,1.924.233c2.944,2.426,6.027,4.851,9.132,7.16a1.884,1.884,0,0,1-.162,3.126,301.407,301.407,0,0,1-45.89,21.83,1.875,1.875,0,0,0-1,2.611,391.055,391.055,0,0,0,30.014,48.815,1.864,1.864,0,0,0,2.063.7A486.048,486.048,0,0,0,610.7,405.729a1.882,1.882,0,0,0,.765-1.352C623.729,277.594,590.933,167.465,524.531,69.836ZM222.491,337.58c-28.972,0-52.844-26.587-52.844-59.239S193.056,219.1,222.491,219.1c29.665,0,53.306,26.82,52.843,59.239C275.334,310.993,251.924,337.58,222.491,337.58Zm195.38,0c-28.971,0-52.843-26.587-52.843-59.239S388.437,219.1,417.871,219.1c29.667,0,53.307,26.82,52.844,59.239C470.715,310.993,447.538,337.58,417.871,337.58Z"/></svg>
          </a>
  
        </div>

        <div class="flex items-align mb-3">

          <Logo />
          <div class="ml-2 h-9 w-[62px] flex -mt-1">
            <img class="w-full" src="/images/midi-link.png" alt="MIDI.link" />
          </div>

        </div>

        <span class="text-xs text-gray-400">
          ????? {new Date().getFullYear()} MIDI.link, All Rights Reserved
        </span>
  
      </div>

      <div class="grid grid-cols-3 gap-8 text-sm text-gray-400">

        <div class="flex flex-col">
          <a class="mb-2" href="#">View NFTs</a>
          <a class="mb-2" href="#">Connect Instrument</a>
          <a href="#">Shopping Cart</a>
        </div>
  
        <div class="flex flex-col">
          <a class="mb-2" href="#">Connect Wallet</a>
          <a class="mb-2" href="#">Supported Devices</a>
          <a href="#">Inquiries</a>
        </div>
  
        <div class="flex flex-col">
          <a class="mb-2" href="#">About</a>
          <a class="mb-2" href="#">Terms</a>
          <a href="#">Privacy</a>
        </div>
  
      </div>

    </div>
    
  </footer>

</main>