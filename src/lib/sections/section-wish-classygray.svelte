<script lang="ts">
  import { ScrollArea } from "$lib/components/ui/scroll-area/index.js";
    let wishes = [
    { name: "Sendvitation", message: "在你们人生最重要的时刻，愿你们的婚姻充满幸福、理解和包容。愿你们在未来的日子里，无论遇到什么困难，都能携手共进，彼此支持。婚姻是一段旅程，需要耐心、信任和爱心。愿你们每天都能发现彼此新的优点，愿你们的家庭充满欢笑和温暖。愿你们的爱情像长江一样源远流长，像泰山一样坚定不移。愿你们的梦想都能实现，愿你们的生活充满阳光和希望。无论风雨还是晴天，愿你们始终相伴，永不分离。祝你们新婚快乐，百年好合，早生贵子，幸福美满，永远相爱，直到永远。在未来的岁月里，愿你们共同经历人生的每一个阶段，无论是喜悦还是挑战，都能彼此扶持，携手前行。愿你们的家庭成为温暖的港湾，让每一位成员都感受到爱与关怀。愿你们在工作中取得成功，在生活中收获满足，在友情中得到支持，在亲情中体会温情。愿你们的每一天都充满希望，每一个梦想都能实现，每一次努力都能得到回报。愿你们的爱情如同春天的花朵，永远盛开；如同秋天的果实，硕果累累。愿你们在旅途中欣赏世界的美丽，在家中享受宁静的时光，在朋友的陪伴下欢笑，在家人的关怀中成长。愿你们的心灵始终相通，无论距离多远，始终牵挂彼此。愿你们的生活充满色彩，像彩虹一样绚烂；愿你们的未来充满希望，像星空一样广阔。愿你们在困难面前不退缩，在成功面前不骄傲，在平凡中发现美好，在忙碌中保持从容。愿你们的婚姻如同一首美丽的诗，句句动人；如同一幅精致的画，色彩斑斓。愿你们的家庭充满欢声笑语，孩子们健康成长，父母们安享晚年。愿你们的事业蒸蒸日上，朋友们真诚相待，邻里和睦相处。愿你们在每一个节日都能团聚，在每一个纪念日都能庆祝，在每一个平凡的日子都能感受到幸福。愿你们的爱情如同大海一样深邃，如同高山一样稳固，如同阳光一样温暖，如同月光一样柔和。愿你们的生活充满智慧与勇气，善良与宽容，信任与理解。愿你们在每一次争吵后都能和解，在每一次误会后都能沟通，在每一次困难后都能携手共度。愿你们在每一个清晨都能感受到新的一天的希望，在每一个夜晚都能彼此依偎，分享心事。愿你们的家庭成为朋友们羡慕的榜样，成为亲人们温暖的依靠。愿你们的孩子聪明健康，愿你们的父母安享晚年。愿你们的事业蒸蒸日上，生活充满乐趣。愿你们在每一次旅行中都能收获美好的回忆，在每一次聚会中都能感受到友情的温暖。愿你们的家中充满欢声笑语，愿你们的生活充满阳光和希望。愿你们在每一个节日都能团聚，在每一个纪念日都能庆祝，在每一个平凡的日子都能感受到幸福。愿你们的爱情如同美酒，越久越香；如同老树，根深叶茂。愿你们的家庭幸福美满，子孙满堂。愿你们的爱情永不褪色，生活永远精彩。祝你们新婚快乐，百年好合，早生贵子，幸福美满，永远相爱，直到永远。" },
    { name: "Sendvitation2", message: "Semoga pernikahan kalian selalu penuh cinta dan berkah" },
    { name: "Dinda Saputra", message: "Turut berbahagia! Semoga langgeng dan selalu rukun" },
    { name: "Raffi Ahmad", message: "Selamat ya, bahagia selalu" },
    { name: "Agnez Mo", message: "Semoga pernikahan kalian selalu penuh cinta dan berkah" },
    { name: "Maudy Ayunda", message: "Turut berbahagia! Semoga langgeng dan selalu rukun" },
    { name: "Nicholas Saputra", message: "Congratulations! Wishing you a lifetime of happiness together." },
    { name: "Ayu Ting Ting", message: "Selamat menempuh hidup baru 🎉" },
    { name: "Joko Widodo", message: "Lorem ipsum dolor sit amet, consectetur adipiscing elit." },
    { name: "Augustus", message: "Vivamus luctus urna sed urna ultricies ac tempor dui sagittis." },
    { name: "Ariel Noah", message: "Doa terbaik untuk kalian berdua. Semoga bahagia hingga akhir hayat." },
    { name: "Bunga Citra Lestari", message: "May your journey ahead be filled with love and laughter ❤️" },
    { name: "Dewi Perssik", message: "Semoga jadi keluarga yang sakinah, mawaddah, warahmah." },
    { name: "Bayu Setiawan", message: "Lorem ipsum dolor sit amet, happy wedding pokoknya!" },
    { name: "Titi DJ", message: "Best wishes! ❤️💍🎉" },
    { name: "Ananta Vinnie", message: "Semoga cepat diberi momongan yaa 😄" },
    { name: "Hamba Allah", message: "Selamat ya, semoga lancar sampai hari H!" },
    { name: "Tamu Virtual", message: "Nullam ut metus id sapien dictum hendrerit nec nec elit." },
    { name: "Fan Bingbing", message: "祝你们新婚快乐，百年好合！" },
    { name: "Jackie Chan", message: "愿你们的生活充满幸福和爱。" },
    { name: "Zhang Ziyi", message: "白头偕老，永结同心。" },
    { name: "Penélope Cruz", message: "¡Felicidades en su boda! Que el amor y la alegría los acompañen siempre." }, // Spanish
    { name: "Omar Sy", message: "Félicitations pour votre mariage ! Tous mes vœux de bonheur." }, // French
    { name: "Heidi Klum", message: "Herzlichen Glückwunsch zur Hochzeit! Alles Gute für eure gemeinsame Zukunft." }, // German
    { name: "Utada Hikaru", message: "ご結婚おめでとうございます。末永くお幸せに。" }, // Japanese
    { name: "Julius Caesar", message: "Amor vincit omnia. Felicitas perpetua vobis!" },
    { name: "Trajan", message: "Vivat amor aeternus inter vos!" },
    { name: "Hadrian", message: "Concordia et fortuna semper vobiscum sit." }
    ];
    $: totalwish = wishes.length;
</script>

<div class="min-h-screen sm:min-h-[1195px] flex flex-col items-center relative p-4 sm:p-10" style="background-image: url(/coverinvertedclassygray.png); background-size: cover; background-position: center; background-repeat: no-repeat;">
    <div class="absolute inset-0 bg-neutral-900/75 items-center justify-center flex flex-col text-neutral-50 px-4 sm:px-0">
        <div class="relative text-center items-center justify-center flex flex-col">
            <h1 class="leading-tight text-4xl md:text-6xl md:p-1" style="font-family: 'Foglihten', serif;">Wish</h1>
        </div>
    
        <!-- Wishes Form -->
        <div class="w-full relative">
            <form class="w-full max-w-xl mx-auto pt-6 flex flex-col gap-1 text-neutral-50">
                <label class="text-lg" for="nama"  style="font-family: 'Cinzel Regular', serif;">Nama Pengirim :</label>
                <input id="nama" name="nama" type="text" placeholder="Nama Tamu"  style="font-family: 'Foglihten Regular', serif;" class="w-full p-3 rounded-md bg-transparent border border-neutral-50 mb-1 placeholder-neutral-50 text-neutral-50" />

                <label class="text-lg" for="pesan"  style="font-family: 'Cinzel Regular', serif;">Message :</label>
                <textarea id="pesan" name="pesan" rows="5" placeholder="Kirim Ucapan"  style="font-family: 'Foglihten Regular', serif;" class="w-full p-3 rounded-md bg-transparent border border-neutral-50 mb-3 sm:mb-6 placeholder-neutral-50 text-neutral-50"></textarea>

                <div class="flex justify-end">
                    <button type="submit" class="px-12 py-1 rounded-lg bg-transparent border border-neutral-50 text-neutral-50 shadow hover:bg-neutral-50 hover:text-neutral-950 transition"  style="font-family: 'Cinzel Regular', serif;">KIRIM</button>
                </div>
            </form>
        </div>

        <!-- Wishes List -->
        <div class="w-full sm:px-8 sm:py-3 text-neutral-50 relative flex flex-col">
            <span class="text-center w-full text-neutral-50 text-lg sm:text-2xl" style="font-family: 'Cinzel Regular', serif;"> {totalwish} Comments</span>
            <ScrollArea class="h-50 sm:h-160 max-h-160 w-full rounded-md" orientation="both">
                {#each wishes as wish}
                <div class="mb-4 md:mb-4 text-left bg-transparent border border-neutral-50 rounded-xl px-4 py-2">
                    <h4 class="text-base md:text-xl sm:mb-3" style="font-family: 'Brittany', cursive;">{wish.name}</h4>
                    <p class="text-justify" style="font-family: 'Cormorant Garamond Regular', cursive;">{wish.message}</p>
                </div>
                {/each}
            </ScrollArea>
        </div>
    </div>
</div>