<template>
   
  
      <header className="w-full flex justify-between items-center p-5">
        <div className="text-left">
          <h1 className="text-3xl font-bold">sint <br />— lukas <br /> bibliotheek</h1>
        </div>
        <nav className="flex gap-6 text-lg font-semibold">
          <Link href="/menu" className="hover:underline">menu</Link>
          <Link href="/search" className="hover:underline">search</Link>
        </nav>
      </header>

      <h2 className="text-6xl font-bold text-orange-500 my-10">contact us</h2>

      <div className="flex flex-col md:flex-row justify-between w-full max-w-4xl text-lg">
        <div>
          <p><strong>LUCA School of Arts</strong></p>
          <p>Bibliotheek Sint-Lukas</p>
          <p>T +32 2 250 11 33</p>
          <p>
            <a href="mailto:bibliotheek.sintlukas@luca-arts.be" className="text-blue-500 underline">
              bibliotheek.sintlukas@luca-arts.be
            </a>
          </p>
        </div>
        <div>
          <p>Paleizenstraat 70</p>
          <p>1030 BRUSSEL</p>
          <p><strong>Opening hours:</strong></p>
          <p>Monday to Friday from 9 am to 6 pm</p>
        </div>
      </div>
      <hr>
      <div class="buttonBack font-bold">
      <NuxtLink to="/books">Access to the collection</NuxtLink>
    </div>
 

</template>
