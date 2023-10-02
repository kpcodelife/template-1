<template>
  <div class="min-h-full relative">
      <PageHeading class="fixed top-[20px] left-[20px]" pageHeading="Showcase" />
      <PageNav class="fixed hidden md:block bottom-[20px] right-[20px]"/>

      <div>
        <ShowCaseItem id="a1" imageSrc="andrey-k-iQeNACvNFVc-unsplash.jpg" heading="Item #1" :description="item1Description" backgroundColor="teal" fontColor="" linkColor=""/>
        <ShowCaseItem id="a2" imageSrc="greg-rosenke-ej5GSCjHXRs-unsplash.jpg" heading="Item #2" :description="item2Description" backgroundColor="orange" fontColor="" linkColor=""/>
        <ShowCaseItem id="a3" imageSrc="marcus-lenk-CH_KY7MK0Jc-unsplash.jpg" heading="Item #3" :description="item2Description" backgroundColor="red" fontColor="" linkColor=""/>
        <ShowCaseItem id="a4" imageSrc="pawel-czerwinski-A_ywJp2bN3w-unsplash.jpg" heading="Item #4" :description="item2Description" backgroundColor="yellow" fontColor="" linkColor=""/>
        <ShowCaseItem id="a5" imageSrc="s-tsuchiya-aXqpGHceDu4-unsplash.jpg" heading="Item #5" :description="item2Description" backgroundColor="blue" fontColor="" linkColor=""/>
      </div>

      <PageDescription class="relative text-center md:text-left md:fixed md:bottom-[100px] md:left-[20px] px-4 md:px-0 mb-12 md:mb-0" :pageDescription="pageDescription" />
      <PagePrivacyPolicy class="relative text-center md:text-left md:fixed md:bottom-[20px] md:left-[20px] px-4 md:px-0 mb-12 md:mb-0" :pagePrivacyText="privacyPolicyText" :pagePrivacyLink="privacyPolicyLink" />
      <PageContact class="relative text-center md:text-left md:fixed md:top-[20px] md:right-[20px] mb-12 md:mb-0" :pageContact="pageContact" />
  </div>
</template>

<script setup>
const item1Description = "This is a brief description about item number 1."
const item2Description = "This is a brief description about item number 2."
const pageDescription = "This is a brief description about item number 2. This is a brief description about item number 2. This is a brief description about item number 2. This is a brief description about item number 2."
const pageContact = "email@thisiscool.com"
const privacyPolicyText = "Privacy Policy"
const privacyPolicyLink = "www.google.com"


</script>
