<script>
    import Card from "./Card.svelte";
    import SocialButton from "./SocialButton.svelte";
</script>

<Card>
    <div class="p-8 flex flex-col gap-[3em] md:flex-row">
        <img src="images/malosdaf.webp" width="256" height="256" class="shadow-xl rounded-[128px] self-center md:self-start" alt="malosdaf"/>
        <div class="flex flex-col gap-0.5">
            <p>{new Date().getFullYear() - 2005}-year old enthusiastic programming student, fonding of science and technology especially mechanical problems</p>
            <p>Main programming languages: <img class="inline h-6" src="images/cpp.svg" alt="c++"> <img class="inline h-6" src="images/csharp.svg" alt="c#"></p>
            <p>Know (kind of) programming languages: <img class="inline h-6" src="images/python.svg" alt="python"> <img class="inline h-6" src="images/java.svg" alt="java"></p>
            <p> Have experience in:
                <img class="inline h-6" src="images/tailwindcss.svg" alt="tailwind">
                <img class="inline h-6" src="images/svelte.svg" alt="svelte">
                <img class="inline h-6" src="images/html5.svg" alt="html5">
                <img class="inline h-6" src="images/bootstrap5.svg" alt="bootstrap5">
                <img class="inline h-6" src="images/netcore.svg" alt="netcore">
                <img class="inline h-6" src="images/sql.svg" alt="sql">
                <img class="inline h-6" src="images/Arduino.svg" alt="Arduino">
            </p>
            <p> IDE:
                <img class="inline h-6" src="images/clion.svg" alt="clion">
                <img class="inline h-6" src="images/pycharm.svg" alt="pycharm">
                <img class="inline h-6" src="images/rider.svg" alt="rider">
                <img class="inline h-6" src="images/webstorm.svg" alt="webstorm">
            </p>
            <p>
                Platform:
                <img class="inline h-6" src="images/window11.svg" alt="window11">

            </p>
            <p>Nationality: <img class="inline h-6 rounded" src="images/vietnam.svg" alt="vietnam"></p>
            <h4 class="my-4">Socials</h4>
            <div class="flex flex-row gap-2">
                <SocialButton src="images/github.svg" alt="github" href="https://github.com/Malosdaf" />
                <SocialButton src="images/twitter.svg" alt="twitter" href="https://twitter.com/doanthienquy1"/>
                <SocialButton src="images/vnoi.webp" alt="vnoi" href="https://oj.vnoi.info/user/Usernoobs"/>
                <SocialButton src="images/cses.webp" alt="cses" href="https://cses.fi/user/33043"/>
            </div>
        </div>
    </div>
</Card>
