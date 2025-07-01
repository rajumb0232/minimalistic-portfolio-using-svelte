<script>
    let testimonials = [
        {
            name: "Prateek Singh",
            company: "iJeeva Software Solutions Pvt Ltd",
            feedback:
                "The project classes by Raju sir are very informative and productive. In detail explanation of each and every concept taught by him helped me a lot in developing my own projects. Training and teaching was great, it was in an interactive and friendly environment where we could discuss to get better understanding of the topic. I landed by first Job because of how well I was clear and thorrow with the concepts taught by Raju sir.",
        },
        {
            name: "Mallikarjun Chonde",
            company: "Travel Hands",
            feedback:
                "The project classes conducted by Raju Sir are excellent. Sir covered all the topics thoroughly and taught us how to apply that knowledge to solve real-world problems. Additionally, we created dedicated real-world projects, which have been very helpful in boosting my career and contributing to my professional growth. Regarding the training, Raju Sir's sessions are excellent. He is knowledgeable, patient, and very calm. His guidance ensures that we learn the latest technologies and understand how to work with them effectively.",
        },
        {
            name: "Nipa Das",
            company: "JMR Infotech",
            feedback:
                "The practical, hands-on approach not only deepened my understanding of Java but also gave me the confidence to apply these skills in real-world scenarios. This training played a crucial role in helping me crack my interview and secure my current position. What I learned during the sessions is now directly benefiting me in my day-to-day work. I’m able to contribute to projects more effectively and solve complex challenges thanks to the strong foundation and practical insights I gained. The skills and knowledge I acquired are continuing to accelerate my career growth.",
        },
        {
            name: "Saurav Kumar",
            company: "Cachatto India Private Limited",
            feedback:
                "The teaching style was clear and easy to understand. You explained every topic in detail, revised regularly, and encouraged active participation with discussions and face-to-face vivas after completing the spring. I improved my thinking ability to answer questions logically and confidently. The focus on explanation, structured notes, and key questions has been very helpful in my career.",
        },
        {
            name: "Muskan",
            company: "Amazon",
            feedback:
                "Best classes with where u get amazing practical knowledge Very helpful and boosts confidence I was able to crack interview because of the training i received from project class",
        },
    ];
</script>

<section class="bg-inherit py-16 px-4 sm:px-6 lg:px-8">
    <div class="max-w-7xl mx-auto">
        <h2 class="text-4xl font-bold text-center mb-2">Testimonials</h2>
        <p class="text-center text-lg mb-10">Mentored 30+ project bootcamps, guiding thousands of corporate
            professionals and aspiring engineering grads. Here’s what some of them had to say 👇</p>

        <div class="grid gap-8 sm:grid-cols-2 lg:grid-cols-3">
            {#each testimonials as testimonial (testimonial.name)}
                <div
                        class="border border-gray-200 hover:border-blue-300 rounded-2xl p-6 hover:scale-105 hover:shadow-[0_0_40px] hover:shadow-blue-300/15 hover:bg-gray-800 transition-all duration-300 ease-in-out"
                >
                    <p class="text-lg text-gray-200 mb-4 line-clamp-6">"{testimonial.feedback}"</p>
                    <div class="mt-4">
                        <p class="font-semibold">{testimonial.name}</p>
                        <p class="text-xs">{testimonial.company}</p>
                    </div>
                </div>
            {/each}
        </div>
    </div>
    <div class="w-full flex justify-end">
        <button
                class="px-8 py-3 bg-blue-600 rounded-xl my-20 hover:bg-blue-700 text-white font-semibold text-lg transition duration-300"
        >
            <a
                    target="_blank"
                    rel="noopener noreferrer"
                    href="https://docs.google.com/spreadsheets/d/1VH_MqM_qRqDX4I3Wwy3VPRdWSqv_hktKEdvL7jaQMOw/edit?usp=sharing"
            >More Testimonials →</a
            >
        </button>
    </div>
</section>
