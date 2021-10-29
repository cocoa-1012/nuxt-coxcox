<template>
  <section class="flex grid grid-cols-2 bg-gray-100 pt-12">
    <div class="flex flex-col items-left justify-center w-4/5 m-auto">
      <p class="text-4xl font-bold">Contact us today</p>
      <div class="bg-yellow-600 w-24 h-2 m-3 ml-28"></div>
      <form id="email-form" name="email-form" data-name="Email Form">
        <input
          id="name"
          type="text"
          class="w-full h-12 my-4 p-4 focus:outline-none rounded"
          maxlength="256"
          name="name"
          data-name="Name"
          placeholder="Name"
        />
        <div class="grid grid-cols-2 gap-4">
          <input
            id="email"
            type="email"
            class="my-2 p-4 focus:outline-none h-12 rounded"
            maxlength="256"
            name="email"
            data-name="Email"
            placeholder="Email"
            required=""
          />
          <input
            id="Phone"
            type="tel"
            class="my-2 p-4 focus:outline-none h-12 rounded"
            maxlength="256"
            name="Phone"
            data-name="Phone"
            placeholder="Phone"
            required=""
          />
        </div>
        <div class="py-4">
          <textarea
            id="Message"
            placeholder="Message"
            maxlength="5000"
            name="Message"
            data-name="Message"
            class="w-full p-4 resize-none focus:outline-none rounded"
            rows="5"
          ></textarea>
        </div>

        <input
          type="submit"
          value="Submit"
          data-wait="Please wait..."
          class="rounded"
        />
      </form>
    </div>
    <div class="column-10 w-col w-col-5">
      <div class="flex items-center w-4/5 h-full">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3456.1739156630233!2d-92.13768718488652!3d29.9744314819078!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x862367f2016092bf%3A0x916bc0c052053c97!2s105%20Tivoli%20St%2C%20Abbeville%2C%20LA%2070510!5e0!3m2!1sen!2sus!4v1634949420130!5m2!1sen!2sus"
          width="100%"
          height="250"
          style="border: 0"
          allowfullscreen=""
          loading="lazy"
        ></iframe>
      </div>
    </div>
  </section>
</template>

<script>
</script> 