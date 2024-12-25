<script>
    import careerCompass from "../../../lib/images/MediaImages/careercompass.jpg";
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
                Career Compass
            </p>
            <div class="text-zinc-600">
                <p>Empowering individuals to navigate their paths with clarity and confidence.</p>
            </div>
        </div>
        <div class="flex justify-center">
            <img src={careerCompass} alt="Career Compass" class="w-96">
        </div>
        <div class="space-y-12">
            <div class="grid grid-cols-3 gap-4 mx-24">
                <p class="text-2xl rasa">Many people struggle to choose a career path due to a lack of access to reliable information, overwhelming choices, and uncertainty about their interests and strengths.</p>
                <p class="col-span-2 text">Research shows that having too many options can lead to decision paralysis, where individuals feel so overwhelmed that they delay making a choice altogether. Recognizing this challenge, Solace Global has developed an innovative database to empower individuals in their career journey. This comprehensive resource offers detailed information about various degrees, professions, and fields of study, all conveniently organized in one place. To make the process even more engaging, each career topic is accompanied by a short video, providing an in-depth look into real-world applications and insights from professionals. By bridging the information gap and simplifying the decision-making process, Solace Global’s initiative helps individuals make informed, confident choices about their futures.</p>
            </div>

            <div class="border-b border-zinc-300 mx-16"></div>

            <!-- Career Dropdowns -->
            <div class="space-y-6 mx-16">
                <!-- Mechanical Engineering -->
                <details class="border rounded-lg shadow p-4">
                    <summary class="cursor-pointer text-2xl rasa">Mechanical Engineering</summary>
                    <div>
                        <div class="text-gray-700 space-y-3">
                            <p class="mt-2 ">
    Mechanical engineering is a foundation of innovation, focusing on designing and developing systems and machinery that power industries and improve lives. From energy-efficient engines and cutting-edge robotics to advanced manufacturing tools, mechanical engineers tackle complex challenges using physics, mathematics, and creativity. This versatile field is vital for advancing transportation, automation, and renewable energy technologies.
                            </p>
                            <p>
    Mechanical engineers also address global challenges like climate change by creating sustainable solutions and improving energy efficiency. With opportunities across industries like aerospace, automotive, and healthcare, this ever-evolving field offers countless ways to shape the future. Check out the video for more information about this exciting career path!
                            </p>
                        </div>
                        <div class="flex justify-center my-6">
                            <iframe width="560" height="315" src="https://www.youtube.com/embed/VlVqBOrKxuE?si=ggNlQHCpTYnvF1Br" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen class="rounded-lg"></iframe>
                        </div>
                    </div>
                </details>

                <!-- Environmental Engineering -->
                <details class="border rounded-lg shadow p-4">
                    <summary class="cursor-pointer text-2xl rasa">Environmental Engineering</summary>
                    <div>
                        <div class="text-gray-700 space-y-3">
                            <p class="mt-2 ">
Environmental engineering addresses critical environmental challenges by designing solutions that protect and preserve the natural world. Combining science and engineering, professionals in this field tackle issues like pollution, waste management, and climate change. They focus on improving air and water quality, managing natural resources, and creating systems that reduce environmental impact, benefiting public health and communities worldwide.
                            </p>
                            <p>
From developing eco-friendly infrastructure to promoting renewable energy, environmental engineers are key to building a sustainable future. Their work helps mitigate climate risks, conserve biodiversity, and promote responsible resource use, making a lasting impact on the planet. Check out the video for more information about this meaningful career path!
                            </p>
                        </div>
                        <div class="flex justify-center my-6">
                            <iframe width="560" height="315" src="https://www.youtube.com/embed/lCtNav7E4n4?si=_DEZlHCQJirjTbXC" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen class="rounded-lg"></iframe>
                        </div>
                    </div>
                </details>

                <!-- Robotics Engineering -->
                <details class="border rounded-lg shadow p-4">
                    <summary class="cursor-pointer text-2xl rasa">Robotics Engineering</summary>
                    <div>
                        <div class="text-gray-700 space-y-3">
                            <p class="mt-2 ">
Robotics engineering merges mechanics, electronics, and software to design advanced robotic systems that transform industries and improve lives. These systems have diverse applications, from manufacturing automation and healthcare robotics to artificial intelligence and space exploration. Robotics engineers push the boundaries of innovation, creating machines that perform tasks with efficiency, precision, and safety.
                            </p>
                            <p>
As technology evolves, robotics engineering offers endless opportunities to revolutionize industries and improve daily life. This cutting-edge field is shaping the future by providing intelligent and adaptable solutions for global challenges. Check out the video for more information about this exciting career path!
                            </p>
                        </div>
                        <div class="flex justify-center my-6">
                            <iframe width="560" height="315" src="https://www.youtube.com/embed/c5wAiNjGbpk?si=fbzhjKcBnbLbpfcA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen class="rounded-lg"></iframe>
                        </div>
                    </div>
                </details>

                <!-- Marine Engineering -->
                <details class="border rounded-lg shadow p-4">
                    <summary class="cursor-pointer text-2xl rasa">Marine Engineering</summary>
                    <div>
                        <div class="text-gray-700 space-y-3">
                            <p class="mt-2 ">
Marine engineering focuses on the design, construction, and maintenance of ships, submarines, and offshore structures. This field plays a crucial role in global commerce, energy exploration, and marine sustainability. Marine engineers face unique challenges, including designing efficient vessels, working in extreme environments, and reducing environmental impacts.
                            </p>
                            <p>
With innovations in propulsion systems and sustainable maritime technologies, marine engineering is vital for advancing ocean exploration and conservation. It ensures the safety and efficiency of maritime operations while addressing environmental concerns. Check out the video for more information about this impactful career path!
                            </p>
                        </div>
                        <div class="flex justify-center my-6">
                            <iframe width="560" height="315" src="https://www.youtube.com/embed/oQryviqD-Q0?si=jPVDyybvlzTZ-i82" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen class="rounded-lg"></iframe>
                        </div>
                    </div>

                </details>

                <!-- Electrical Engineering -->
                <details class="border rounded-lg shadow p-4">
                    <summary class="cursor-pointer text-2xl rasa">Electrical Engineering</summary>
                    <div>
                        <div class="text-gray-700 space-y-3">
                            <p class="mt-2 ">
Electrical engineering is a dynamic field focused on the study and application of electricity, electronics, and electromagnetism. Electrical engineers design systems that power modern life, from consumer electronics to telecommunications and renewable energy. Their work drives advancements in robotics, automation, and energy efficiency.
                            </p>
                            <p>
As technology advances, electrical engineers are central to shaping infrastructure and creating sustainable solutions. This field offers opportunities to develop innovations that improve everyday life and solve global challenges. Check out the video for more information about this impactful career path!
                        </div>
                        <div class="flex justify-center my-6">
                            <iframe width="560" height="315" src="https://www.youtube.com/embed/7cTaS_B-C78?si=TUxphFw9IjVnyfHi" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen class="rounded-lg"></iframe>
                        </div>
                    </div>
                </details>

                <!-- Computer Science -->
                <details class="border rounded-lg shadow p-4">
                    <summary class="cursor-pointer text-2xl rasa">Computer Science</summary>
                    <div>
                        <div class="text-gray-700 space-y-3">
                            <p class="mt-2 ">
Computer science explores programming, algorithms, and computational theory to create innovative solutions for modern challenges. This field underpins advancements in artificial intelligence, cybersecurity, and big data, impacting industries like healthcare, finance, and entertainment. Computer scientists design and optimize systems that transform how we interact with technology.
                            </p>
                            <p>
With its fast-paced evolution, computer science offers opportunities to drive innovation and solve global problems through creativity and technical expertise. This field is essential for shaping the future of technology and its applications. Check out the video for more information about this fascinating career path!                            </p>
                        </div>
                        <div class="flex justify-center my-6">
                            <iframe width="560" height="315" src="https://www.youtube.com/embed/1PrZjjb69qI?si=7uT3vEpu75XF-GX2" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen class="rounded-lg"></iframe>
                        </div>
                    </div>
                </details>


            </div>
        </div>
    </div>
</main>
