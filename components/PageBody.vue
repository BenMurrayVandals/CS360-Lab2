<template>
  <div class="flex flex-col justify-start gap-y-4 grow w-full p-16 bg-slate-600">
    <h1 class="text-white text-4xl font-bold">{{ title }}</h1>
    <p class="text-slate-200 text-sm whitespace-pre-line">
      {{ description }}
    </p>
    <div v-if="title === 'Contact'" class="flex justify-around">
      <div>
        <iframe
          width="523"
          height="403"
          frameborder="0"
          scrolling="no"
          marginheight="0"
          marginwidth="0"
          id="gmap_canvas"
          src="https://maps.google.com/maps?width=523&amp;height=403&amp;hl=en&amp;q=%20Ilford+()&amp;t=&amp;z=12&amp;ie=UTF8&amp;iwloc=B&amp;output=embed"
        ></iframe>
      </div>
      <form class="flex flex-col gap-y-2 w-1/2">
        <div class="flex flex-col">
          <label for="fname" class="text-white">First Name</label>
          <input type="text" id="fname" name="firstname" placeholder="Your name.." class="p-2" />
        </div>
        <div class="flex flex-col">
          <label for="lname" class="text-white">Last Name</label>
          <input type="text" id="lname" name="lastname" placeholder="Your last name.." class="p-2" />
        </div>
        <div class="flex flex-col">
          <label for="country" class="text-white">Country</label>
          <select id="country" name="country" class="p-2">
            <option value="australia">Australia</option>
            <option value="canada">Canada</option>
            <option value="usa">USA</option>
          </select>
        </div>
        <div class="flex flex-col">
          <label for="subject" class="text-white">Subject</label>
          <textarea id="subject" name="subject" placeholder="Write something.." class="h-[200px] p-2"></textarea>
        </div>

        <button
          type="submit"
          class="text-white font-bold bg-slate-800 w-fit py-2 px-4 rounded-lg transition-colors duration-200 hover:bg-slate-900"
        >
          Signup
        </button>
      </form>
    </div>
    <form v-if="title === 'Signin'" class="flex flex-col gap-y-2 w-1/2">
      <div class="flex flex-col">
        <label for="uname" class="text-white"><b>Username</b></label>
        <input type="text" placeholder="Enter Username" name="uname" class="p-2" required />
      </div>
      <div class="flex flex-col">
        <label for="psw" class="text-white"><b>Password</b></label>
        <input type="password" placeholder="Enter Password" name="psw" class="p-2" required />
      </div>

      <button
        type="submit"
        class="text-white font-bold bg-slate-800 w-fit py-2 px-4 rounded-lg transition-colors duration-200 hover:bg-slate-900"
      >
        Login
      </button>
    </form>
    <form v-else-if="title === 'Signup'" class="flex flex-col gap-y-2 w-1/2">
      <div class="flex flex-col">
        <label for="uname" class="text-white"><b>Username</b></label>
        <input type="text" placeholder="Enter Username" name="uname" class="p-2" required />
      </div>
      <div class="flex flex-col">
        <label for="psw" class="text-white"><b>Password</b></label>
        <input type="password" placeholder="Enter Password" name="psw" class="p-2" required />
      </div>

      <button
        type="submit"
        class="text-white font-bold bg-slate-800 w-fit py-2 px-4 rounded-lg transition-colors duration-200 hover:bg-slate-900"
      >
        Signup
      </button>
    </form>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  title: string;
}>();

const description = `Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Quis vel eros donec ac odio tempor. Nunc mattis enim ut tellus. Mauris in aliquam sem fringilla ut morbi tincidunt augue interdum. Amet risus nullam eget felis eget. Viverra adipiscing at in tellus integer feugiat. Eu facilisis sed odio morbi quis commodo odio. A diam maecenas sed enim ut sem viverra aliquet eget. Enim neque volutpat ac tincidunt vitae. Dictum sit amet justo donec enim diam vulputate.

Dui id ornare arcu odio ut sem nulla pharetra. Et netus et malesuada fames. Justo nec ultrices dui sapien eget mi. In nibh mauris cursus mattis molestie. Quam id leo in vitae turpis massa sed elementum tempus. Risus commodo viverra maecenas accumsan. Eget duis at tellus at urna condimentum. Velit ut tortor pretium viverra suspendisse potenti nullam ac. Lobortis scelerisque fermentum dui faucibus in ornare quam. Risus sed vulputate odio ut. Et odio pellentesque diam volutpat commodo sed egestas egestas. Faucibus et molestie ac feugiat sed lectus vestibulum mattis. Lacus sed viverra tellus in hac habitasse. Ipsum suspendisse ultrices gravida dictum fusce ut placerat. Risus nec feugiat in fermentum posuere urna nec. Facilisi etiam dignissim diam quis enim lobortis scelerisque fermentum.

Sed sed risus pretium quam vulputate dignissim suspendisse in est. Aliquam sem fringilla ut morbi tincidunt augue interdum velit. Orci nulla pellentesque dignissim enim sit amet venenatis urna cursus. Pulvinar sapien et ligula ullamcorper malesuada proin libero nunc consequat. Auctor neque vitae tempus quam pellentesque. Ut tristique et egestas quis ipsum suspendisse ultrices gravida. Nunc faucibus a pellentesque sit amet porttitor eget. Pharetra sit amet aliquam id diam maecenas ultricies. Ut tristique et egestas quis ipsum. In nulla posuere sollicitudin aliquam ultrices sagittis. Blandit cursus risus at ultrices mi tempus imperdiet nulla malesuada. Nibh nisl condimentum id venenatis a. Sed risus pretium quam vulputate dignissim suspendisse. Eget est lorem ipsum dolor sit amet consectetur. Dolor magna eget est lorem. Erat velit scelerisque in dictum non consectetur a.

Rutrum tellus pellentesque eu tincidunt tortor aliquam nulla facilisi cras. Magna eget est lorem ipsum dolor sit amet consectetur adipiscing. Vel eros donec ac odio tempor orci dapibus ultrices. Nisl vel pretium lectus quam. Lorem dolor sed viverra ipsum nunc aliquet bibendum enim facilisis. A iaculis at erat pellentesque adipiscing. Fringilla ut morbi tincidunt augue interdum velit euismod in pellentesque. Id venenatis a condimentum vitae. Facilisi etiam dignissim diam quis enim. Commodo viverra maecenas accumsan lacus vel facilisis volutpat est. Quis viverra nibh cras pulvinar mattis nunc sed blandit libero. Mauris in aliquam sem fringilla. Amet consectetur adipiscing elit ut aliquam. Maecenas ultricies mi eget mauris pharetra. Massa massa ultricies mi quis hendrerit.

Leo in vitae turpis massa sed elementum tempus. Lobortis scelerisque fermentum dui faucibus. Faucibus et molestie ac feugiat sed lectus. Faucibus interdum posuere lorem ipsum dolor sit amet consectetur. Vulputate sapien nec sagittis aliquam malesuada bibendum arcu vitae. At ultrices mi tempus imperdiet. Orci ac auctor augue mauris augue neque. Fringilla ut morbi tincidunt augue interdum velit euismod. Sagittis aliquam malesuada bibendum arcu. Est ullamcorper eget nulla facilisi etiam dignissim diam quis enim. Quisque sagittis purus sit amet volutpat consequat mauris nunc congue. Risus at ultrices mi tempus imperdiet nulla. Fringilla ut morbi tincidunt augue interdum velit. Sit amet nisl suscipit adipiscing bibendum est ultricies integer quis. Neque laoreet suspendisse interdum consectetur libero. Magna fringilla urna porttitor rhoncus dolor purus non enim. Vitae semper quis lectus nulla at volutpat diam ut venenatis. Et ligula ullamcorper malesuada proin. Quam pellentesque nec nam aliquam sem et tortor consequat. Sed odio morbi quis commodo odio aenean.`;
</script>
