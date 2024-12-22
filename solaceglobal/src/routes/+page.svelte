<script>
    import Icon from "../lib/images/SolaceGlobalLogo.png";
    import Video from "../lib/images/ActualActualFinalVideo.mp4";
    import ArticleImage from "../lib/images/article1.png";
    import PartnersImage from "../lib/images/PartnersImage.png";


</script>

<main>
    <div class="flex h-full">
        <div class="flex-grow"></div>
        <!-- Content Div -->
        <div class="flex-shrink-0 w-[1200px]">
            <nav class="w-full py-4 border-b">
                <div class="grid grid-cols-3 items-center px-4 w-full">
                    <!-- Logo -->
                    <div class="flex justify-start">
                        <a href="/">
                            <img src={Icon} alt="Logo" class="w-32">
                        </a>
                    </div>
                    <!-- Links -->
                    <div class="flex justify-center space-x-8">
                        <a href="/" class="text-lg font-medium hover:text-black hover:underline">About Us</a>
                        <a href="/" class="text-lg font-medium hover:text-black hover:underline">Our Work</a>
                        <a href="/" class="text-lg font-medium hover:text-black hover:underline">Ideas</a>
                    </div>
                    <!-- Donate -->
                    <div class="flex justify-end">
                        <a href="/" class="text-lg hover:text-black hover:underline">Donate</a>
                    </div>
                </div>
            </nav>
            <!-- Hero Div -->
            <div class="mt-16 px-8">
                <!-- Slogan- Unite to create a future of lasting value -->
                <h1 class="text-6xl  font-medium w-[800px] leading-[4.5rem] ">
                    Unite to create a future of lasting value
                </h1>
                <!-- Hyperlinked Text under slogan- Learn about empowerment and innovation to create lasting change for tomorrow. -->
                <p class="mt-5 text-xl border-b-2 w-[725px]  border-black">
                    <a href="/">
                        Learn about empowerment and innovation to create lasting change for tomorrow.
                    </a>
                </p>
            </div>
            <!-- Video- 3 frame video  -->
            <div class="mt-20">
                <video loop muted autoplay poster={Icon} width="1920">
                    <source src={Video} type="video/mp4">
                </video>
                    <!-- Hyperlink Text under video- Discover Solace Globals Philanthropy  to explore giving opportunities and make an impact. -->
                <p class="mt-5 text-md font-medium underline px-8">
                    <a href="/">
                        Discover Solace Globals Philanthropy to explore giving opportunities and make an impact
                    </a>
                </p>
            </div>
            <!-- Featured Insights - article names - chess is a catalyst for knowledge, how ai effects education, robotics, climate change  -->
            <div class="mt-12">
                <div>
                    <p class="text-3xl font-medium">
                        Featured Insights
                    </p>
                </div>
                <div class="grid grid-cols-4 gap-4 mt-12">
                    <div class="w-64 hover:underline"><img src={ArticleImage} alt="ArticleImage" class="w-64"> <div class="mt-4"><span class="font-bold">Article</span> Chess is a Catalyst for Knowledge</div></div>
                    <div class="w-64 hover:underline"><img src={ArticleImage} alt="ArticleImage" class="w-64"> <div class="mt-4"><span class="font-bold">Article</span> How AI Effects Education</div></div>
                    <div class="w-64 hover:underline"><img src={ArticleImage} alt="ArticleImage" class="w-64"> <div class="mt-4"><span class="font-bold">Article</span> Robotics</div></div>
                    <div class="w-64 hover:underline"><img src={ArticleImage} alt="ArticleImage" class="w-64"> <div class="mt-4"><span class="font-bold">Article</span> Climate Change</div></div>
                </div>
            </div>
            
            
            <div class="my-16 border-t-2"></div>

        <!-- Partners of Solace Global- has text - How does the work of our partners come to life? How does that work create potential around the world? Watch, read, and experience the stories of good people doing great things that can lead to even greater things. -->
            <div class="grid grid-cols-3">
                <div class="col-span-2">
                    <img src={PartnersImage} alt="Partners" class="">
                </div>
                <div class="">
                    <p class="text-3xl py-8  text-center">Partners of Solace Global</p>
                </div>
            </div>
        <!-- End of Content Div -->
        </div>
        <div class="flex-grow"></div>
    </div>
</main>



<!-- Button under Partners of Solace Global (learn more)-  Legacy Homes, Project World Impact,Undefined Robotics, pinkberry, hackclub, shanti bhavan, + info -->
<!-- Perspectives- Explore the latest updates, research, and stories from the foundation, Solace Global weekly updates newsletter. -->
<!-- Learn More Perspectives top right button- BLACK PAGE Latest update on importance issues offering diverse insights around the world, image with quote - Knowledge is the light that guides us through the darkness., under image - title - Unlocking true understanding through knowledge and impartiality. Next to image have newsletter subscription, 10 articles not on main page under image and newsletter. Videos under not on main page, under that have another sign up for newsletter(Subscribe to the The Wisdom), Partners again, -->
<!-- Foundation Facts- 6650+ people affected, 3400+ - money, 50+ students, 11+ programs  -->
