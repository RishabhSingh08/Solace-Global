<script>

    import image01 from "../../../lib/images/MediaImages/IMG_6224.jpg";
    import image02 from "../../../lib/images/MediaImages/kids.jpg";
    import image03 from "../../../lib/images/MediaImages/IMG_6585 (1).jpg";
    import image04 from "../../../lib/images/MediaImages/IMG_6596.jpg";
    import image05 from "../../../lib/images/MediaImages/IMG_6589.jpg";

</script>

<svelte:head>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Caveat:wght@400..700&family=Rasa:ital,wght@0,300..700;1,300..700&display=swap" rel="stylesheet">
</svelte:head>
<style>
.rasa {
  font-family: "Rasa", serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
}
</style>



<main>
    <div class="space-y-12">
        <!-- FAQ Header -->
        <div class="text-center space-y-2">
            <p class="text-6xl rasa font-bold text-black">
                The Discovery Project
            </p>
            <div class="text-zinc-600">
                <p>The Discovery Project empowers individuals to explore new ideas and cultivate </p>
                <p>curiosity through hands-on learning experiences across various fields.</p>
            </div>
        </div>
        <div>
            <img src="https://placehold.co/1920x1080" alt="">
        </div>
        <div class="space-y-12 ">
        <div class="grid grid-cols-3 gap-4 mx-24">
            <div class="text-2xl rasa space-y-4">

                <p class="italic">"I think, at a child's birth, if a mother could ask a fairy godmother to endow it with the most useful gift, that gift would be curiosity,"</p><p>— Eleanor Roosevelt.
    </p>
            </div>
            <p class="col-span-2 text"> The Discovery Project is an initiative designed to inspire curiosity and foster innovation by providing individuals with opportunities to explore new ideas and concepts across various fields. Through hands-on experiences and engaging activities, the project encourages participants to step outside their comfort zones, challenge their thinking, and develop a deeper understanding of the world around them. By combining education with exploration, the Discovery Project aims to ignite a passion for learning, spark creativity, and empower individuals to think critically and pursue their interests with confidence. Whether through STEM-related activities, art, or other disciplines, the Discovery Project is dedicated to unlocking the potential of every participant and inspiring the next generation of thinkers, creators, and problem-solvers.
</p>
        </div>

        <div class="border-b border-zinc-300 mx-16"></div>
        <div id="dreams" class="space-y-6">

            <div class="grid grid-cols-9 gap-8 items-center">
                <div class="space-y-5 col-span-4 ">
                    <p class="text-3xl rasa text-justify" >
                3D Dreams: Empowering Kids
                    </p>
</div>
                <div class="col-span-5">
                </div>
            </div>
        </div>
        <div class="border-b border-zinc-300 mx-16"></div>
        <div id="robots" class="space-y-6">
            <div class="grid grid-cols-9 gap-16 items-center">
                <div class="col-span-5">
        

                <div class="grid grid-cols-2 gap-3">
                    <img src={image02} alt="kids">
                    <img src={image04} alt="kids">
                    <img src={image05} alt="kids">
                    <img src={image03} alt="kids">
                </div>


                        
                </div>
                <div class="space-y-5 col-span-4">
                <p class="text-3xl rasa" >Robots for Earth</p>
                <p>The event aimed to teach kids about climate change through the lens of robotics, led by a UTD researcher with expertise in 3D autonomous systems. It began with an informative presentation that explained how robotics can address environmental issues, such as waste management and pollution. The presentation highlighted the potential of technology in solving climate change-related problems and set the stage for the hands-on activities that followed.</p>
                <p>Participants had the opportunity to build and program a SPARK Prime robot—created by a member of the Undefined Robotics team—that autonomously cleaned trash using a claw mechanism. This practical experience allowed the kids to apply what they had learned during the presentation and see how robotics can be utilized to tackle real-world sustainability challenges.</p>
                <p>Through this hands-on activity, participants not only learned basic robotics skills but also gained an understanding of how innovation can be used to reduce pollution and promote environmental conservation. The event sparked creativity and encouraged the kids to think about how technology can help protect the planet. By combining interactive learning and an educational presentation, the event empowered the next generation to explore how they can contribute to combating climate change through robotics and other technological solutions.</p>
            </div>
            </div>
        </div>
        <div class="border-b border-zinc-300 mx-16"></div>
        <div id="seniors" class="space-y-6">

            <div class="grid grid-cols-9 gap-8 items-center">
                <div class="space-y-5 col-span-4 ">
                    <p class="text-3xl rasa text-justify" >
Smart Seniors                    </p>
</div>
    </div>
            <div class="border-b border-zinc-300 mx-16"></div>
        <div id="spark" class="space-y-6">
            <div class="grid grid-cols-9 gap-16 items-center">
                <div class="col-span-4">
        

                    <div class="text-center text-sm my-4 space-y-4">
                        <img src={image01} alt="team">
                    </div>
                        
                </div>
                <div class="space-y-5 col-span-5">
                <p class="text-3xl rasa" >
                    STEM Spark
                </p>
                <p>
Led by members of a STATE UIL-winning robotics team and a World FTC Qualifying team, this event in Plano, Texas, provided an engaging and immersive hands-on experience designed to inspire the next generation of innovators and leaders in STEM. Participants explored a range of science and technology concepts through interactive activities that sparked curiosity and creativity, offering a perspective often missing from traditional school settings. By engaging with high school students, who acted as mentors and role models, the event created a "big brother" effect, where younger participants felt more connected and open to asking questions, experimenting, and thinking critically.
                </p>
                <p>
                    The activities encouraged children to think outside the box, experiment with new ideas, and approach problems in creative ways, all while fostering a passion for learning and innovation. The experience gave them the opportunity to explore robotics and technology in a relaxed, supportive environment, where learning felt less like a classroom and more like an exciting challenge. By introducing these young minds to real-world applications of science and technology, the event inspired them to consider how innovation can solve pressing global issues. Ultimately, it paved the way for future leaders in STEM by providing both technical knowledge and a deeper sense of possibility that traditional schooling often doesn't offer.
                </p>
                </div>
            </div>
        </div>
        <!-- Main FAQ Content -->
    </div>
</main>
