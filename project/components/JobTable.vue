<template>
  <table class="min-w-full leading-normal">
    <thead>
      <tr>
        <th
          class="px-5 py-3 border-b-2 border-gray-200 bg-gray-100 text-left text-xs font-semibold text-gray-600 uppercase tracking-wider"
        >
          Company
        </th>
        <th
          class="px-5 py-3 border-b-2 border-gray-200 bg-gray-100 text-left text-xs font-semibold text-gray-600 uppercase tracking-wider"
        >
          Role
        </th>
        <th
          class="px-5 py-3 border-b-2 border-gray-200 bg-gray-100 text-left text-xs font-semibold text-gray-600 uppercase tracking-wider"
        >
          Location
        </th>
        <th
          class="px-5 py-3 border-b-2 border-gray-200 bg-gray-100 text-left text-xs font-semibold text-gray-600 uppercase tracking-wider"
        >
          Link
        </th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="job of jobs" :key="job">
        <td class="px-5 py-5 border-b border-gray-200 bg-white text-sm">
          <div class="flex items-center">
            <div class="flex-shrink-0 w-10 h-10">
              <img
                class="w-full h-full rounded-full"
                :src="job.img"
                alt=""
              >
            </div>
            <div class="ml-3">
              <p class="text-gray-900 whitespace-no-wrap">
                {{ job.company }}
              </p>
            </div>
          </div>
        </td>
        <td class="px-5 py-5 border-b border-gray-200 bg-white text-sm">
          <p class="text-gray-900 whitespace-no-wrap">
            {{ job.role }}
          </p>
        </td>
        <td class="px-5 py-5 border-b border-gray-200 bg-white text-sm">
          <p class="text-gray-900 whitespace-no-wrap">
            {{ job.location }}
          </p>
        </td>
        <td class="px-5 py-5 border-b border-gray-200 bg-white text-sm">
          <span
            class="relative inline-block px-3 py-1 font-semibold text-blue-500 leading-tight"
          >
            <span
              aria-hidden
              class="absolute inset-0 bg-blue-200 opacity-50 rounded-full"
            />
            <span class="relative"><a :href="job.link">Apply</a></span>
          </span>
        </td>
      </tr>
    </tbody>
  </table>
</template>

<script>
export default {
  data () {
    return {
      jobs: [
        {
          img: 'https://pbs.twimg.com/profile_images/1305899202703048705/bMHePt35_400x400.png',
          company: 'Facebook',
          role: 'Software Engineer, Intern/Co-op',
          location: 'London, United Kingdom',
          link: 'https://www.facebook.com/careers/jobs/1716969328451048'
        },
        {
          img: 'https://pbs.twimg.com/profile_images/806220210239926272/1YQ70tXT_400x400.jpg',
          company: 'Amazon',
          role: 'Software Development Engineer Internship',
          location: 'London, UK',
          link: 'https://www.amazon.jobs/en/jobs/1271918/software-development-engineer-internship-london-uk'
        },
        {
          img: 'https://pbs.twimg.com/profile_images/1268191541941559296/GOQb6uBi_400x400.png',
          company: 'Microsoft',
          role: 'Software Engineering Internship',
          location: 'UK: London and Cambridge',
          link: 'https://careers.microsoft.com/us/en/job/878093/Intern-Opportunities-for-Students-UK-Software-Engineering'
        },
        {
          img: 'https://pbs.twimg.com/profile_images/1192935671473659905/AMUy2VsJ_400x400.jpg',
          company: 'Slack',
          role: 'Software Engineering Internship',
          location: 'Remote Internship',
          link: 'https://slack.com/intl/en-gb/careers/2322106/software-engineering-internship'
        }
      ]
    }
  }
}
</script>

<style>
</style>
