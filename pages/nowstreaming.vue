<template>
  <div class="container movies">
    <MoviesGrid style="color: white;">
      <MovieCard v-for="(movie, index) in movies" :key="index" :movie="movie"/>
      <!-- <div v-for="(movie, index) in movies" :key="index" class="movie">{{movie}}</div> -->
      <!-- <div v-for="x in [1,2,3,4,5,6,7,8,9,10]" :key="x">{{x}}. Hello</div> -->
    </MoviesGrid>
  </div>
  <!-- <div>
    <h1>Hello</h1>
  </div>-->
</template>

<script>
import MovieCard from "@/components/MovieCard.vue"
import MoviesGrid from "@/components/MoviesGrid.vue"


export default {
  components: { MoviesGrid, MovieCard },
  data() {
    return {
      movies: [
        {
          adult: false,
          backdrop_path: '/8Y43POKjjKDGI9MH89NW0NAzzp8.jpg',
          genre_ids: [35, 28, 12, 878],
          id: 550988,
          original_language: 'en',
          original_title: 'Free Guy',
          overview: 'A bank teller called Guy realizes he is a background character in an open world video game called Free City that will soon go offline.',
          popularity: 7508.219,
          poster_path: '/xmbU4JTUm8rsdtn7Y3Fcm30GpeT.jpg',
          release_date: '2021-08-11',
          title: 'Free Guy',
          video: false,
          vote_average: 7.9,
          vote_count: 2285
        },
        {
          adult: false,
          backdrop_path: '/t9nyF3r0WAlJ7Kr6xcRYI4jr9jm.jpg',
          genre_ids: [878, 28],
          id: 580489,
          original_language: 'en',
          original_title: 'Venom: Let There Be Carnage',
          overview: 'After finding a host body in investigative reporter Eddie Brock, the alien symbiote must face a new enemy, Carnage, the alter ego of serial killer Cletus Kasady.',
          popularity: 8830.327,
          poster_path: '/rjkmN1dniUHVYAtwuV3Tji7FsDO.jpg',
          release_date: '2021-09-30',
          title: 'Venom: Let There Be Carnage',
          video: false,
          vote_average: 7.5,
          vote_count: 239
        },
        {
          adult: false,
          backdrop_path: '/aO9Nnv9GdwiPdkNO79TISlQ5bbG.jpg',
          genre_ids: [28, 12],
          id: 568620,
          original_language: 'en',
          original_title: 'Snake Eyes: G.I. Joe Origins',
          overview: "After saving the life of their heir apparent, tenacious loner Snake Eyes is welcomed into an ancient Japanese clan called the Arashikage where he is taught the ways of the ninja warrior. But, when secrets from his past are revealed, Snake Eyes' honor and allegiance will be tested – even if that means losing the trust of those closest to him.",
          popularity: 3553.668,
          poster_path: '/uIXF0sQGXOxQhbaEaKOi2VYlIL0.jpg',
          release_date: '2021-07-22',
          title: 'Snake Eyes: G.I. Joe Origins',
          video: false,
          vote_average: 6.9,
          vote_count: 586
        },
        {
          adult: false,
          backdrop_path: '/cinER0ESG0eJ49kXlExM0MEWGxW.jpg',
          genre_ids: [28, 12, 14],
          id: 566525,
          original_language: 'en',
          original_title: 'Shang-Chi and the Legend of the Ten Rings',
          overview: 'Shang-Chi must confront the past he thought he left behind when he is drawn into the web of the mysterious Ten Rings organization.',
          popularity: 1446.101,
          poster_path: '/1BIoJGKbXjdFDAqUEiA2VHqkK1Z.jpg',
          release_date: '2021-09-01',
          title: 'Shang-Chi and the Legend of the Ten Rings',
          video: false,
          vote_average: 7.8,
          vote_count: 1203
        },
        {
          adult: false,
          backdrop_path: '/iDLtDgxLiYsarfdQ4msUhUqoNPp.jpg',
          genre_ids: [878],
          id: 725273,
          original_language: 'en',
          original_title: 'Solitary',
          overview: "A man wakes up inside a room to discover he's a prisoner sent into space to form Earth's first colony, and worse - his cell mate Alana is hell bent on destroying everything.",
          popularity: 1417.641,
          poster_path: '/ApwmbrMlsuOay5rXQA4Kbz7qJAl.jpg',
          release_date: '2021-09-24',
          title: 'Solitary',
          video: false,
          vote_average: 6.7,
          vote_count: 31
        },
        {
          adult: false,
          backdrop_path: '/7WJjFviFBffEJvkAms4uWwbcVUk.jpg',
          genre_ids: [12, 14, 35, 28],
          id: 451048,
          original_language: 'en',
          original_title: 'Jungle Cruise',
          overview: 'Dr. Lily Houghton enlists the aid of wisecracking skipper Frank Wolff to take her down the Amazon in his dilapidated boat. Together, they search for an ancient tree that holds the power to heal – a discovery that will change the future of medicine.',
          popularity: 1142.244,
          poster_path: '/9dKCd55IuTT5QRs989m9Qlb7d2B.jpg',
          release_date: '2021-07-28',
          title: 'Jungle Cruise',
          video: false,
          vote_average: 7.8,
          vote_count: 2865
        },
        {
          adult: false,
          backdrop_path: '/kTOheVmqSBDIRGrQLv2SiSc89os.jpg',
          genre_ids: [16, 35, 10751],
          id: 639721,
          original_language: 'en',
          original_title: 'The Addams Family 2',
          overview: 'The Addams get tangled up in more wacky adventures and find themselves involved in hilarious run-ins with all sorts of unsuspecting characters.',
          popularity: 1077.877,
          poster_path: '/xYLBgw7dHyEqmcrSk2Sq3asuSq5.jpg',
          release_date: '2021-10-01',
          title: 'The Addams Family 2',
          video: false,
          vote_average: 7.9,
          vote_count: 151
        },
        {
          adult: false,
          backdrop_path: '/aT0XL7YLDx9GfpU2q8kgWUtn0on.jpg',
          genre_ids: [28, 80, 53],
          id: 385128,
          original_language: 'en',
          original_title: 'F9',
          overview: "Dominic Toretto and his crew battle the most skilled assassin and high-performance driver they've ever encountered: his forsaken brother.",
          popularity: 1058.802,
          poster_path: '/bOFaAXmWWXC3Rbv4u4uM9ZSzRXP.jpg',
          release_date: '2021-05-19',
          title: 'F9',
          video: false,
          vote_average: 7.5,
          vote_count: 3955
        },
        {
          adult: false,
          backdrop_path: '/3GgkzCDq6KYpcmJmcOKh27hYRyj.jpg',
          genre_ids: [12, 16, 10751, 14],
          id: 588921,
          original_language: 'en',
          original_title: 'Ainbo: Spirit of the Amazon',
          overview: `An epic journey of a young hero and her Spirit Guides, 'Dillo' a cute and humorous armadillo and "Vaca" a goofy oversized tapir, who embark on a quest to save their home in the spectacular Amazon Rainforest.`,
          popularity: 924.312,
          poster_path: '/l8HyObVj8fPrzacAPtGWWLDhcfh.jpg',
          release_date: '2021-02-09',
          title: 'Ainbo: Spirit of the Amazon',
          video: false,
          vote_average: 7.2,
          vote_count: 187
        },
        {
          adult: false,
          backdrop_path: '/pUc51UUQb1lMLVVkDCaZVsCo37U.jpg',
          genre_ids: [53, 27],
          id: 482373,
          original_language: 'en',
          original_title: "Don't Breathe 2",
          overview: 'The Blind Man has been hiding out for several years in an isolated cabin and has taken in and raised a young girl orphaned from a devastating house fire. Their quiet life together is shattered when a group of criminals kidnap the girl, forcing the Blind Man to leave his safe haven to save her.',
          popularity: 841.293,
          poster_path: '/hRMfgGFRAZIlvwVWy8DYJdLTpvN.jpg',
          release_date: '2021-08-12',
          title: "Don't Breathe 2",
          video: false,
          vote_average: 7.7,
          vote_count: 902
        },
        {
          adult: false,
          backdrop_path: '/MDYanFolbT76dj0gsCbhS2GM5A.jpg',
          genre_ids: [37, 28],
          id: 859860,
          original_language: 'en',
          original_title: 'Catch the Bullet',
          overview: 'U.S. marshal Britt MacMasters returns from a mission to find his father wounded and his son kidnapped by the outlaw Jed Blake. Hot on their trail, Britt forms a posse with a gunslinging deputy and a stoic Pawnee tracker. But Jed and Britt tread dangerously close to the Red Desert’s Sioux territory.',
          popularity: 913.414,
          poster_path: '/qKxrBZ8Ts4KHZKp7BT6GAVMLFO2.jpg',
          release_date: '2021-09-10',
          title: 'Catch the Bullet',
          video: false,
          vote_average: 5.8,
          vote_count: 50
        },
        {
          adult: false,
          backdrop_path: '/ugukqzx4gSzBd1yzmbWEHLkpGaS.jpg',
          genre_ids: [16, 10751, 14, 35, 10402, 12],
          id: 597316,
          original_language: 'en',
          original_title: 'My Little Pony: A New Generation',
          overview: "Equestria's divided. But a bright-eyed hero believes Earth Ponies, Pegasi and Unicorns should be pals — and, hoof to heart, she’s determined to prove it.",
          popularity: 882.715,
          poster_path: '/hzq5XRGgm6NDMOW1idUvbpGqEkv.jpg',
          release_date: '2021-09-23',
          title: 'My Little Pony: A New Generation',
          video: false,
          vote_average: 8,
          vote_count: 84
        },
        {
          adult: false,
          backdrop_path: '/akwg1s7hV5ljeSYFfkw7hTHjVqk.jpg',
          genre_ids: [16, 35, 12, 10751],
          id: 459151,
          original_language: 'en',
          original_title: 'The Boss Baby: Family Business',
          overview: 'The Templeton brothers — Tim and his Boss Baby little bro Ted — have become adults and drifted away from each other. But a new boss baby with a cutting-edge approach and a can-do attitude is about to bring them together again … and inspire a new family business.',
          popularity: 911.891,
          poster_path: '/uWStkK8bq9ixY3fc7y209ZleCoF.jpg',
          release_date: '2021-07-01',
          title: 'The Boss Baby: Family Business',
          video: false,
          vote_average: 7.7,
          vote_count: 1475
        },
        {
          adult: false,
          backdrop_path: '/mtRW6eAwOO27h3zrfU2foQFW7Hg.jpg',
          genre_ids: [16, 10751, 12, 35],
          id: 675445,
          original_language: 'en',
          original_title: 'PAW Patrol: The Movie',
          overview: 'Ryder and the pups are called to Adventure City to stop Mayor Humdinger from turning the bustling metropolis into a state of chaos.',
          popularity: 842.706,
          poster_path: '/ic0intvXZSfBlYPIvWXpU1ivUCO.jpg',
          release_date: '2021-08-09',
          title: 'PAW Patrol: The Movie',
          video: false,
          vote_average: 7.8,
          vote_count: 571
        },
        {
          adult: false,
          backdrop_path: '/8s4h9friP6Ci3adRGahHARVd76E.jpg',
          genre_ids: [16, 35, 10751, 878],
          id: 379686,
          original_language: 'en',
          original_title: 'Space Jam: A New Legacy',
          overview: "When LeBron and his young son Dom are trapped in a digital space by a rogue A.I., LeBron must get them home safe by leading Bugs, Lola Bunny and the whole gang of notoriously undisciplined Looney Tunes to victory over the A.I.'s digitized champions on the court. It's Tunes versus Goons in the highest-stakes challenge of his life.",
          popularity: 801.316,
          poster_path: '/5bFK5d3mVTAvBCXi5NPWH0tYjKl.jpg',
          release_date: '2021-07-08',
          title: 'Space Jam: A New Legacy',
          video: false,
          vote_average: 7.3,
          vote_count: 2362
        },
        {
          adult: false,
          backdrop_path: '/byflnwPMumyvrCW9SfO5Miq3647.jpg',
          genre_ids: [28, 53],
          id: 597891,
          original_language: 'en',
          original_title: 'Kate',
          overview: "After she's irreversibly poisoned, a ruthless criminal operative has less than 24 hours to exact revenge on her enemies and in the process forms an unexpected bond with the daughter of one of her past victims.",
          popularity: 819.572,
          poster_path: '/uJgdT1boTSP0dDIjdTgGleg71l4.jpg',
          release_date: '2021-09-10',
          title: 'Kate',
          video: false,
          vote_average: 6.8,
          vote_count: 599
        },
        {
          adult: false,
          backdrop_path: '/qD45xHA35HdJDGOaA1AgDwiWEgO.jpg',
          genre_ids: [10749, 18],
          id: 744275,
          original_language: 'en',
          original_title: 'After We Fell',
          overview: "Just as Tessa's life begins to become unglued, nothing is what she thought it would be. Not her friends nor her family. The only person that she should be able to rely on is Hardin, who is furious when he discovers the massive secret that she's been keeping. Before Tessa makes the biggest decision of her life, everything changes because of revelations about her family.",
          popularity: 712.182,
          poster_path: '/3WfvjNWr5k1Zzww81b3GWc8KQhb.jpg',
          release_date: '2021-09-01',
          title: 'After We Fell',
          video: false,
          vote_average: 8.1,
          vote_count: 318
        },
        {
          adult: false,
          backdrop_path: '/gzppdxEJ6fofhtLzSVSUJZEVxvq.jpg',
          genre_ids: [28, 878, 53],
          id: 848278,
          original_language: 'en',
          original_title: 'Jurassic Hunt',
          overview: 'Female adventurer Parker joins a crew of male trophy hunters in a remote wilderness park. Their goal: slaughter genetically recreated dinosaurs for sport using rifles, arrows, and grenades. After their guide is killed by raptors, the team tries to escape the park – but the hunters quickly become the hunted. Even worse, the park’s manager suspects Parker of being a spy and sends a hit squad after her. This battle’s about to become primitive!',
          popularity: 693.613,
          poster_path: '/bZnOioDq1ldaxKfUoj3DenHU7mp.jpg',
          release_date: '2021-08-26',
          title: 'Jurassic Hunt',
          video: false,
          vote_average: 4.9,
          vote_count: 143
        },
        {
          adult: false,
          backdrop_path: '/u5Fp9GBy9W8fqkuGfLBuuoJf57Z.jpg',
          genre_ids: [12, 28, 53],
          id: 370172,
          original_language: 'en',
          original_title: 'No Time to Die',
          overview: 'Bond has left active service and is enjoying a tranquil life in Jamaica. His peace is short-lived when his old friend Felix Leiter from the CIA turns up asking for help. The mission to rescue a kidnapped scientist turns out to be far more treacherous than expected, leading Bond onto the trail of a mysterious villain armed with dangerous new technology.',
          popularity: 610.966,
          poster_path: '/eqWaeh21e4ZgHjwpULZVHCGIq9X.jpg',
          release_date: '2021-09-29',
          title: 'No Time to Die',
          video: false,
          vote_average: 7.3,
          vote_count: 355
        },
        {
          adult: false,
          backdrop_path: '/70AV2Xx5FQYj20labp0EGdbjI6E.jpg',
          genre_ids: [28, 80, 53],
          id: 637649,
          original_language: 'en',
          original_title: 'Wrath of Man',
          overview: "A cold and mysterious new security guard for a Los Angeles cash truck company surprises his co-workers when he unleashes precision skills during a heist. The crew is left wondering who he is and where he came from. Soon, the marksman's ultimate motive becomes clear as he takes dramatic and irrevocable steps to settle a score.",
          popularity: 567.887,
          poster_path: '/M7SUK85sKjaStg4TKhlAVyGlz3.jpg',
          release_date: '2021-04-22',
          title: 'Wrath of Man',
          video: false,
          vote_average: 7.8,
          vote_count: 2375
        }
      ],
    }
  }
}
</script>

<style>
</style>
