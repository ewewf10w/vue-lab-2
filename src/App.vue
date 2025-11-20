<script setup>
const peoples = [
  {
    name: 'Steve',
    tag: 'Boss',
    tagline: 'your favourite coffee daily lives tempor.',
    image: '/images/team/portrait-elegant-old-man-wearing-suit.jpg',
  },
  {
    name: 'Sandra',
    tag: 'Manager',
    tagline: 'your favourite coffee daily lives.',
    image:
      '/images/team/cute-korean-barista-girl-pouring-coffee-prepare-filter-batch-brew-pour-working-cafe.jpg',
  },
  {
    name: 'Jackson',
    tag: 'Senior',
    tagline: 'your favourite coffee daily lives.',
    image: '/images/team/small-business-owner-drinking-coffee.jpg',
  },
  {
    name: 'Michelle',
    tag: 'Barista',
    tagline: 'your favourite coffee daily consectetur.',
    image: '/images/team/smiley-business-woman-working-cashier.jpg',
  },
];

const menus = [
  {
    name: 'Breakfast',
    type: 'Delicious Menu',
    items: [
      {
        name: 'Pancakes',
        price: '$12.50',
        oldPrice: null,
        descr: 'Fresh brewed coffee and steamed milk',
        isRecommended: false,
      },
      {
        name: 'Toasted Waffle',
        price: '$12.00',
        oldPrice: '$16.50',
        descr: 'Brewed coffee and steamed milk',
        isRecommended: false,
      },
      {
        name: 'Fried Chips',
        price: '$15.0',
        oldPrice: null,
        descr: 'Rich Milk and Foam',
        isRecommended: true,
      },
      {
        name: 'Pecan Pancakes',
        price: '$15.50',
        oldPrice: '$33.33',
        descr: 'Studded with lots of nuts, pecan pancakes',
        isRecommended: false,
      },
      {
        name: 'Banana Cakes',
        price: '$18.0',
        oldPrice: null,
        descr: 'Studded with lots of nuts, pecan pancakes',
        isRecommended: false,
      },
    ],
  },
  {
    name: 'Coffee',
    type: 'Favourite Menu',
    items: [
      {
        name: 'Latte',
        price: '$7.50',
        oldPrice: '$12.50',
        descr: 'Fresh brewed coffee and steamed milk',
        isRecommended: false,
      },
      {
        name: 'White Coffee',
        price: '$5.90',
        oldPrice: null,
        descr: 'Brewed coffee and steamed milk',
        isRecommended: true,
      },
      {
        name: 'Chocolate Milk',
        price: '$5.50',
        oldPrice: null,
        descr: 'Rich Milk and Foam',
        isRecommended: false,
      },
      {
        name: 'Greentea',
        price: '$7.50',
        oldPrice: null,
        descr: 'Fresh brewed coffee and steamed milk',
        isRecommended: false,
      },
      {
        name: 'Dark Chocolate',
        price: '$7.25',
        oldPrice: null,
        descr: 'Rich Milk and Foam',
        isRecommended: false,
      },
    ],
  },
];

const testimonials = [
  {
    author: {
      name: 'Sandra',
      who: 'Customers',
      avatar: '/images/reviews/young-woman-with-round-glasses-yellow-sweater.jpg',
    },
    rating: '2',
    descr:
      'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
  },
  {
    author: {
      name: 'Don',
      who: 'Customers',
      avatar: '/images/reviews/senior-man-white-sweater-eyeglasses.jpg',
    },
    rating: '3.5',
    descr:
      'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
  },
  {
    author: {
      name: 'Olivia',
      who: 'Customers',
      avatar:
        '/images/reviews/young-beautiful-woman-pink-warm-sweater-natural-look-smiling-portrait-isolated-long-hair.jpg',
    },
    rating: '5',
    descr:
      'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
  },
  {
    author: {
      name: 'John',
      who: 'Customers',
      avatar: '/images/reviews/young-woman-with-round-glasses-yellow-sweater.jpg',
    },
    rating: '4.5',
    descr:
      'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
  },
];

const generateStarsClass = (rating) => {
  const starsClass = [];
  const fullStars = Math.floor(rating); // Количество полных звезд
  const hasHalfStar = rating % 1 >= 0.5; // Нужна ли половина звезды

  for (let i = 0; i < fullStars; i++) {
    starsClass.push('bi-star-fill');
  }

  if (hasHalfStar) {
    starsClass.push('bi-star-half');
  }

  const emptyStars = 5 - fullStars - (hasHalfStar ? 1 : 0);
  for (let i = 0; i < emptyStars; i++) {
    starsClass.push('bi-star');
  }

  return starsClass;
};
</script>

<template>
  <main>
    <section class="hero-section d-flex justify-content-center align-items-center" id="section_1">
      <div class="container">
        <div class="row align-items-center">
          <div class="col-lg-6 col-12 mx-auto">
            <em class="small-text">welcome tasddo Barista.co</em>

            <h1>Cafe Klang</h1>

            <p class="text-white mb-4 pb-lg-2">your <em>favourite</em> coffee daily lives.</p>

            <a class="btn custom-btn custom-border-btn smoothscroll me-3" href="#section_2">
              Our Story
            </a>

            <a class="btn custom-btn smoothscroll me-2 mb-2" href="#section_3"
              ><strong>Check Menu</strong></a
            >
          </div>
        </div>
      </div>
    </section>

    <section class="about-section section-padding" id="section_2">
      <div class="section-overlay"></div>
      <div class="container">
        <div class="row align-items-center">
          <div class="col-lg-6 col-12">
            <div class="ratio ratio-1x1">
              <video autoplay="" loop="" muted="" class="custom-video" poster="">
                <source src="/videos/pexels-mike-jones-9046237.mp4" type="video/mp4" />

                Your browser does not support the video tag.
              </video>

              <div class="about-video-info d-flex flex-column">
                <h4 class="mt-auto">We Started Since 2009.</h4>

                <h4>Best Cafe in Klang.</h4>
              </div>
            </div>
          </div>

          <div class="col-lg-5 col-12 mt-4 mt-lg-0 mx-auto">
            <em class="text-white">Barista.co</em>

            <h2 class="text-white mb-3">Cafe KL</h2>

            <p class="text-white">
              The café had been in the town for as long as anyone could remember, and it had become
              a beloved institution among the locals.
            </p>

            <p class="text-white">
              The café was run by a friendly and hospitable couple, Mr. and Mrs. Johnson. Barista
              Cafe is free Bootstrap 5 HTML layout provided by
              <a rel="nofollow" href="https://www.tooplate.com" target="_blank">Tooplate</a>.
            </p>

            <a href="#barista-team" class="smoothscroll btn custom-btn custom-border-btn mt-3 mb-4"
              >Meet Baristas</a
            >
          </div>
        </div>
      </div>
    </section>

    <section class="barista-section section-padding section-bg" id="barista-team">
      <div class="container">
        <div class="row justify-content-center">
          <div class="col-lg-12 col-12 text-center mb-4 pb-lg-2">
            <em class="text-white">Creative Baristas</em>

            <h2 class="text-white">Meet People</h2>
          </div>

          <div
            v-for="people in peoples"
            :key="people.name + people.tag"
            class="col-lg-3 col-md-6 col-12 mb-4"
          >
            <div class="team-block-wrap">
              <div class="team-block-info d-flex flex-column">
                <div class="d-flex mt-auto mb-3">
                  <h4 class="text-white mb-0">{{ people.name }}</h4>

                  <p class="badge ms-4">
                    <em>{{ people.tag }}</em>
                  </p>
                </div>

                <p class="text-white mb-0">{{ people.tagline }}</p>
              </div>

              <div class="team-block-image-wrap">
                <img :src="people.image" class="team-block-image img-fluid" alt="" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="menu-section section-padding" id="section_3">
      <div class="container">
        <!-- mb-4 mb-lg-0 -->
        <div class="row">
          <div v-for="menu of menus" :key="menu.name + menu.type" class="col-lg-6 col-12">
            <div class="menu-block-wrap">
              <div class="text-center mb-4 pb-lg-2">
                <em class="text-white">{{ menu.name }}</em>
                <h4 class="text-white">{{ menu.type }}</h4>
              </div>

              <div v-for="item of menu.items" :key="item.name" class="menu-block my-4">
                <div class="d-flex">
                  <h6>
                    {{ item.name }}
                    <span v-if="item.isRecommended" class="badge ms-3">Recommend</span>
                  </h6>

                  <span class="underline"></span>
                  <div class="ms-auto">
                    <strong v-if="item.oldPrice" class="text-white ms-auto"
                      ><s>{{ item.oldPrice }}</s></strong
                    >

                    <strong class="ms-2">{{ item.price }}</strong>
                  </div>
                </div>

                <div class="border-top mt-2 pt-2">
                  <small>{{ item.descr }}</small>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="reviews-section section-padding section-bg" id="section_4">
      <div class="container">
        <div class="row justify-content-center">
          <div class="col-lg-12 col-12 text-center mb-4 pb-lg-2">
            <em class="text-white">Reviews by Customers</em>

            <h2 class="text-white">Testimonials</h2>
          </div>

          <div class="timeline">
            <template v-for="(testimonial, index) of testimonials" :key="testimonial.author.name">
              <div
                :class="{ 'timeline-container-right': index % 2 == 1 }"
                class="timeline-container"
              >
                <div class="timeline-content">
                  <div class="reviews-block">
                    <div class="reviews-block-image-wrap d-flex align-items-center">
                      <img
                        :src="testimonial.author.avatar"
                        class="reviews-block-image img-fluid"
                        alt=""
                      />

                      <div>
                        <h6 class="text-white mb-0">{{ testimonial.author.name }}</h6>
                        <em class="text-white"> {{ testimonial.author.who }}</em>
                      </div>
                    </div>

                    <div class="reviews-block-info">
                      <p>
                        {{ testimonial.descr }}
                      </p>

                      <div class="d-flex border-top pt-3 mt-4">
                        <strong class="text-white"
                          >{{ testimonial.rating }} <small class="ms-2">Rating</small></strong
                        >

                        <div class="reviews-group ms-auto">
                          <i
                            :class="starClass"
                            v-for="starClass of generateStarsClass(testimonial.rating)"
                          ></i>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </template>
          </div>
        </div>
      </div>
    </section>

    <section class="contact-section section-padding" id="section_5">
      <div class="container">
        <div class="row">
          <div class="col-lg-12 col-12">
            <em class="text-white">Say Hello</em>
            <h2 class="text-white mb-4 pb-lg-2">Contact</h2>
          </div>

          <div class="col-lg-6 col-12">
            <form action="#" method="post" class="custom-form contact-form" role="form">
              <div class="row">
                <div class="col-lg-6 col-12">
                  <label for="name" class="form-label">Name <sup class="text-danger">*</sup></label>

                  <input
                    type="text"
                    name="name"
                    id="name"
                    class="form-control"
                    placeholder="Jackson"
                    required=""
                  />
                </div>

                <div class="col-lg-6 col-12">
                  <label for="email" class="form-label">Email Address</label>

                  <input
                    type="email"
                    name="email"
                    id="email"
                    class="form-control"
                    placeholder="Jack@gmail.com"
                    required=""
                  />
                </div>

                <div class="col-12">
                  <label for="message" class="form-label">How can we help?</label>

                  <textarea
                    name="message"
                    rows="4"
                    class="form-control"
                    id="message"
                    placeholder="Message"
                    required=""
                  ></textarea>
                </div>
              </div>

              <div class="col-lg-5 col-12 mx-auto mt-3">
                <button type="submit" class="form-control">Send Message</button>
              </div>
            </form>
          </div>

          <div class="col-lg-6 col-12 mx-auto mt-5 mt-lg-0 ps-lg-5">
            <iframe
              class="google-map"
              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d5039.668141741662!2d72.81814769288509!3d19.043340656729775!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3be7c994f34a7355%3A0x2680d63a6f7e33c2!2sLover%20Point!5e1!3m2!1sen!2sth!4v1692722771770!5m2!1sen!2sth"
              width="100%"
              height="300"
              style="border: 0"
              allowfullscreen=""
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"
            ></iframe>
          </div>
        </div>
      </div>
    </section>

    <footer class="site-footer">
      <div class="container">
        <div class="row">
          <div class="col-lg-4 col-12 me-auto">
            <em class="text-white d-block mb-4">Where to find us?</em>

            <strong class="text-white">
              <i class="bi-geo-alt me-2"></i>
              Bandra West, Mumbai, Maharashtra 400050, India
            </strong>

            <ul class="social-icon mt-4">
              <li class="social-icon-item">
                <a href="#" class="social-icon-link bi-facebook"> </a>
              </li>

              <li class="social-icon-item">
                <a href="https://x.com/minthu" target="_new" class="social-icon-link bi-twitter">
                </a>
              </li>

              <li class="social-icon-item">
                <a href="#" class="social-icon-link bi-whatsapp"> </a>
              </li>
            </ul>
          </div>

          <div class="col-lg-3 col-12 mt-4 mb-3 mt-lg-0 mb-lg-0">
            <em class="text-white d-block mb-4">Contact</em>

            <p class="d-flex mb-1">
              <strong class="me-2">Phone:</strong>
              <a href="tel: 305-240-9671" class="site-footer-link"> (65) 305 2409 671 </a>
            </p>

            <p class="d-flex">
              <strong class="me-2">Email:</strong>

              <a href="mailto:info@yourgmail.com" class="site-footer-link"> hello@barista.co </a>
            </p>
          </div>

          <div class="col-lg-5 col-12">
            <em class="text-white d-block mb-4">Opening Hours.</em>

            <ul class="opening-hours-list">
              <li class="d-flex">
                Monday - Friday
                <span class="underline"></span>

                <strong>9:00 - 18:00</strong>
              </li>

              <li class="d-flex">
                Saturday
                <span class="underline"></span>

                <strong>11:00 - 16:30</strong>
              </li>

              <li class="d-flex">
                Sunday
                <span class="underline"></span>

                <strong>Closed</strong>
              </li>
            </ul>
          </div>

          <div class="col-lg-8 col-12 mt-4">
            <p class="copyright-text mb-0">
              Copyright © Barista Cafe 2048 - Design:
              <a rel="sponsored" href="https://www.tooplate.com" target="_blank">Tooplate</a>
            </p>
          </div>
        </div>
      </div>
    </footer>
  </main>
</template>
