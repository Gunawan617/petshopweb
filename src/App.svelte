<script>
  let isMenuOpen = false;
  
  const services = [
    {
      title: 'Makanan Kucing',
      desc: 'Berbagai pilihan makanan berkualitas untuk kucing kesayangan Anda',
      icon: 'food',
      color: '#14b8a6'
    },
    {
      title: 'Adopsi',
      desc: 'Temukan teman berbulu baru untuk keluarga Anda',
      icon: 'adopt',
      color: '#f97316'
    },
    {
      title: 'Shelter',
      desc: 'Tempat aman dan nyaman untuk hewan peliharaan',
      icon: 'shelter',
      color: '#8b5cf6'
    },
    {
      title: 'Grooming',
      desc: 'Perawatan profesional untuk penampilan terbaik hewan Anda',
      icon: 'grooming',
      color: '#ec4899'
    }
  ];

  const products = [
    {
      name: 'Royal Canin Kitten',
      price: 'Rp 125.000',
      image: 'https://images.unsplash.com/photo-1589924691995-400dc9ecc119?w=500&q=80',
      category: 'Makanan',
      rating: 4.8
    },
    {
      name: 'Whiskas Adult',
      price: 'Rp 85.000',
      image: 'https://images.unsplash.com/photo-1591871937573-74dbba515c4c?w=500&q=80',
      category: 'Makanan',
      rating: 4.5
    },
    {
      name: 'Pro Plan Sensitive',
      price: 'Rp 145.000',
      image: 'https://images.unsplash.com/photo-1548681528-6a5c45b66b42?w=500&q=80',
      category: 'Makanan',
      rating: 4.9
    },
    {
      name: 'Me-O Persian',
      price: 'Rp 95.000',
      image: 'https://images.unsplash.com/photo-1516750930508-dd9ba78b7d3f?w=500&q=80',
      category: 'Makanan',
      rating: 4.6
    }
  ];

  const testimonials = [
    {
      name: 'Sarah Johnson',
      role: 'Cat Owner',
      image: 'https://images.unsplash.com/photo-1494790108377-be9c29b29330?w=200&q=80',
      rating: 5,
      text: 'Pelayanan grooming sangat profesional! Kucing saya jadi lebih sehat dan bersih. Highly recommended!'
    },
    {
      name: 'Michael Chen',
      role: 'Dog Owner',
      image: 'https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=200&q=80',
      rating: 5,
      text: 'Makanan yang dijual berkualitas tinggi dan harga terjangkau. Anjing saya sangat suka!'
    },
    {
      name: 'Diana Putri',
      role: 'Pet Adopter',
      image: 'https://images.unsplash.com/photo-1438761681033-6461ffad8d80?w=200&q=80',
      rating: 5,
      text: 'Berhasil adopsi kucing dari sini. Prosesnya mudah dan staffnya sangat membantu. Thank you Paws!'
    }
  ];

  const gallery = [
    {
      image: 'https://images.unsplash.com/photo-1574158622682-e40e69881006?w=600&q=80',
      title: 'Grooming Session',
      category: 'Grooming'
    },
    {
      image: 'https://images.unsplash.com/photo-1583337130417-3346a1be7dee?w=600&q=80',
      title: 'Happy Cats',
      category: 'Shelter'
    },
    {
      image: 'https://images.unsplash.com/photo-1548681528-6a5c45b66b42?w=600&q=80',
      title: 'Premium Products',
      category: 'Products'
    },
    {
      image: 'https://images.unsplash.com/photo-1573865526739-10c1dd7aa5d0?w=600&q=80',
      title: 'Adoption Day',
      category: 'Adoption'
    },
    {
      image: 'https://images.unsplash.com/photo-1495360010541-f48722b34f7d?w=600&q=80',
      title: 'Playtime',
      category: 'Shelter'
    },
    {
      image: 'https://images.unsplash.com/photo-1519052537078-e6302a4968d4?w=600&q=80',
      title: 'After Grooming',
      category: 'Grooming'
    }
  ];

  const faqs = [
    {
      question: 'Apakah produk makanan dijamin original?',
      answer: 'Ya, semua produk makanan yang kami jual 100% original dan memiliki sertifikat resmi dari distributor.'
    },
    {
      question: 'Berapa lama proses grooming?',
      answer: 'Proses grooming biasanya memakan waktu 2-3 jam tergantung jenis layanan dan kondisi hewan peliharaan Anda.'
    },
    {
      question: 'Bagaimana cara adopsi hewan?',
      answer: 'Anda bisa datang langsung ke toko kami, pilih hewan yang ingin diadopsi, isi formulir, dan tim kami akan membantu proses selanjutnya.'
    },
    {
      question: 'Apakah ada layanan konsultasi dokter hewan?',
      answer: 'Ya, kami memiliki dokter hewan yang siap berkonsultasi setiap hari Senin-Jumat pukul 10.00-17.00 WIB.'
    },
    {
      question: 'Berapa biaya shelter per hari?',
      answer: 'Biaya shelter mulai dari Rp 50.000/hari sudah termasuk makanan dan perawatan dasar. Ada paket mingguan dan bulanan dengan harga lebih hemat.'
    }
  ];

  let openFaqIndex = null;

  function toggleFaq(index) {
    openFaqIndex = openFaqIndex === index ? null : index;
  }

  const whatsappNumber = '6281234567890';
  const whatsappMessage = 'Halo, saya tertarik dengan layanan Paws Petshop';
  
  function openWhatsApp() {
    const url = `https://wa.me/${whatsappNumber}?text=${encodeURIComponent(whatsappMessage)}`;
    window.open(url, '_blank');
  }
</script>

<main>
  <!-- Navbar -->
  <nav class="navbar">
    <div class="nav-container">
      <div class="logo">
        <div class="logo-circle">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
            <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm0 18c-4.41 0-8-3.59-8-8s3.59-8 8-8 8 3.59 8 8-3.59 8-8 8z"/>
            <circle cx="8.5" cy="10.5" r="1.5"/>
            <circle cx="15.5" cy="10.5" r="1.5"/>
            <path d="M8.5 14.5c1 1.5 2.5 2 3.5 2s2.5-.5 3.5-2"/>
          </svg>
        </div>
        <span class="logo-text">Paws</span>
      </div>
      <button class="menu-toggle" on:click={() => isMenuOpen = !isMenuOpen}>
        <span></span>
        <span></span>
        <span></span>
      </button>
      <ul class="nav-links" class:active={isMenuOpen}>
        <li><a href="#home">Home</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#products">Products</a></li>
        <li><a href="#contact">Contact</a></li>
        <li><button on:click={openWhatsApp} class="nav-cta">Get Started</button></li>
      </ul>
    </div>
  </nav>

  <!-- Hero Section -->
  <section class="hero" id="home">
    <div class="hero-left">
      <div class="hero-badge">Premium Pet Care</div>
      <h1 class="hero-title">
        Your Pet's<br/>
        <span class="title-highlight">Happy Place</span>
      </h1>
      <p class="hero-text">
        Kami menyediakan makanan berkualitas, layanan adopsi, shelter nyaman, 
        dan grooming profesional untuk hewan kesayangan Anda.
      </p>
      <div class="hero-stats">
        <div class="stat-item">
          <div class="stat-number">500+</div>
          <div class="stat-label">Happy Pets</div>
        </div>
        <div class="stat-item">
          <div class="stat-number">50+</div>
          <div class="stat-label">Adopted</div>
        </div>
        <div class="stat-item">
          <div class="stat-number">4.9</div>
          <div class="stat-label">Rating</div>
        </div>
      </div>
      <div class="hero-actions">
        <a href="#services" class="btn-hero-primary">Explore Services</a>
        <button on:click={openWhatsApp} class="btn-hero-secondary">
          <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
            <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm0 18c-4.41 0-8-3.59-8-8s3.59-8 8-8 8 3.59 8 8-3.59 8-8 8z"/>
            <path d="M13 7h-2v5H7v2h4v4h2v-4h4v-2h-4z"/>
          </svg>
          Contact Us
        </button>
      </div>
    </div>
    <div class="hero-right">
      <div class="hero-image-wrapper">
        <img src="https://images.unsplash.com/photo-1514888286974-6c03e2ca1dba?w=800&q=80" alt="Cute Cat" class="hero-main-image"/>
        <div class="floating-card card-1">
          <svg width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M18 8h1a4 4 0 010 8h-1M2 8h16v9a4 4 0 01-4 4H6a4 4 0 01-4-4V8z"/>
            <line x1="6" y1="1" x2="6" y2="4"/>
            <line x1="10" y1="1" x2="10" y2="4"/>
            <line x1="14" y1="1" x2="14" y2="4"/>
          </svg>
          <div class="card-text">Premium Food</div>
        </div>
        <div class="floating-card card-2">
          <svg width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M22 11.08V12a10 10 0 11-5.93-9.14"/>
            <polyline points="22 4 12 14.01 9 11.01"/>
          </svg>
          <div class="card-text">Healthy & Happy</div>
        </div>
      </div>
    </div>
  </section>

  <!-- Services Section -->
  <section id="services" class="services-section">
    <div class="section-header">
      <span class="section-label">What We Offer</span>
      <h2 class="section-title-large">Our Services</h2>
    </div>
    
    <div class="services-asymmetric">
      {#each services as service, index}
        <div class="service-box" style="--service-color: {service.color}">
          <div class="service-number">0{index + 1}</div>
          <div class="service-icon-wrapper">
            {#if service.icon === 'food'}
              <svg width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <path d="M18 8h1a4 4 0 010 8h-1M2 8h16v9a4 4 0 01-4 4H6a4 4 0 01-4-4V8z"/>
                <line x1="6" y1="1" x2="6" y2="4"/>
                <line x1="10" y1="1" x2="10" y2="4"/>
                <line x1="14" y1="1" x2="14" y2="4"/>
              </svg>
            {:else if service.icon === 'adopt'}
              <svg width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <path d="M20.84 4.61a5.5 5.5 0 00-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 00-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 000-7.78z"/>
              </svg>
            {:else if service.icon === 'shelter'}
              <svg width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <path d="M3 9l9-7 9 7v11a2 2 0 01-2 2H5a2 2 0 01-2-2z"/>
                <polyline points="9 22 9 12 15 12 15 22"/>
              </svg>
            {:else if service.icon === 'grooming'}
              <svg width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <path d="M14.7 6.3a1 1 0 000 1.4l1.6 1.6a1 1 0 001.4 0l3.77-3.77a6 6 0 01-7.94 7.94l-6.91 6.91a2.12 2.12 0 01-3-3l6.91-6.91a6 6 0 017.94-7.94l-3.76 3.76z"/>
              </svg>
            {/if}
          </div>
          <h3 class="service-title">{service.title}</h3>
          <p class="service-desc">{service.desc}</p>
          <a href="#contact" class="service-link">Learn More →</a>
        </div>
      {/each}
    </div>
  </section>

  <!-- Products Section -->
  <section id="products" class="products-section">
    <div class="section-header-center">
      <span class="section-label">Best Sellers</span>
      <h2 class="section-title-large">Premium Products</h2>
      <p class="section-subtitle">Makanan berkualitas tinggi untuk kucing kesayangan Anda</p>
    </div>
    
    <div class="products-overlap">
      {#each products as product, index}
        <div class="product-overlap-card" style="--index: {index}">
          <div class="product-img-container">
            <img src={product.image} alt={product.name} />
            <div class="product-overlay">
              <button class="btn-quick-view">Quick View</button>
            </div>
          </div>
          <div class="product-info">
            <div class="product-header">
              <span class="product-category">{product.category}</span>
              <div class="product-rating">
                <svg width="16" height="16" viewBox="0 0 24 24" fill="#fbbf24">
                  <path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/>
                </svg>
                <span>{product.rating}</span>
              </div>
            </div>
            <h3 class="product-name">{product.name}</h3>
            <div class="product-footer">
              <span class="product-price">{product.price}</span>
              <button class="btn-add-cart">
                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                  <circle cx="9" cy="21" r="1"/>
                  <circle cx="20" cy="21" r="1"/>
                  <path d="M1 1h4l2.68 13.39a2 2 0 002 1.61h9.72a2 2 0 002-1.61L23 6H6"/>
                </svg>
              </button>
            </div>
          </div>
        </div>
      {/each}
    </div>
  </section>

  <!-- Testimonials Section -->
  <section class="testimonials-section">
    <div class="section-header-center">
      <span class="section-label">What They Say</span>
      <h2 class="section-title-large">Happy Customers</h2>
      <p class="section-subtitle">Dengar cerita dari customer kami yang puas</p>
    </div>
    
    <div class="testimonials-grid">
      {#each testimonials as testimonial}
        <div class="testimonial-card">
          <div class="testimonial-header">
            <img src={testimonial.image} alt={testimonial.name} class="testimonial-avatar"/>
            <div class="testimonial-info">
              <h4 class="testimonial-name">{testimonial.name}</h4>
              <p class="testimonial-role">{testimonial.role}</p>
            </div>
          </div>
          <div class="testimonial-rating">
            {#each Array(testimonial.rating) as _, i}
              <svg width="18" height="18" viewBox="0 0 24 24" fill="#fbbf24">
                <path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/>
              </svg>
            {/each}
          </div>
          <p class="testimonial-text">"{testimonial.text}"</p>
        </div>
      {/each}
    </div>
  </section>

  <!-- Gallery Section -->
  <section class="gallery-section">
    <div class="section-header-center">
      <span class="section-label">Our Gallery</span>
      <h2 class="section-title-large">Moments We Love</h2>
      <p class="section-subtitle">Lihat momen bahagia hewan peliharaan di Paws</p>
    </div>
    
    <div class="gallery-grid">
      {#each gallery as item, index}
        <div class="gallery-item" style="--delay: {index * 0.1}s">
          <img src={item.image} alt={item.title} />
          <div class="gallery-overlay">
            <span class="gallery-category">{item.category}</span>
            <h3 class="gallery-title">{item.title}</h3>
          </div>
        </div>
      {/each}
    </div>
  </section>

  <!-- FAQ Section -->
  <section class="faq-section">
    <div class="faq-container">
      <div class="faq-left">
        <span class="section-label">FAQ</span>
        <h2 class="section-title-large">Frequently Asked Questions</h2>
        <p class="faq-intro">Punya pertanyaan? Kami punya jawabannya. Jika tidak menemukan jawaban yang Anda cari, jangan ragu untuk menghubungi kami.</p>
        <button on:click={openWhatsApp} class="btn-faq-contact">
          <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
            <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413Z"/>
          </svg>
          Contact Us
        </button>
      </div>
      
      <div class="faq-right">
        {#each faqs as faq, index}
          <div class="faq-item" class:active={openFaqIndex === index}>
            <button class="faq-question" on:click={() => toggleFaq(index)}>
              <span>{faq.question}</span>
              <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" class="faq-icon">
                <polyline points="6 9 12 15 18 9"/>
              </svg>
            </button>
            <div class="faq-answer">
              <p>{faq.answer}</p>
            </div>
          </div>
        {/each}
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="contact-section">
    <div class="contact-grid">
      <div class="contact-content">
        <span class="section-label">Get In Touch</span>
        <h2 class="section-title-large">Visit Our Store</h2>
        <p class="contact-intro">Kunjungi toko kami atau hubungi untuk informasi lebih lanjut tentang layanan dan produk kami.</p>
        
        <div class="contact-details">
          <div class="detail-row">
            <div class="detail-icon" style="background: #14b8a6;">
              <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="2">
                <path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0118 0z"/>
                <circle cx="12" cy="10" r="3"/>
              </svg>
            </div>
            <div class="detail-text">
              <div class="detail-label">Address</div>
              <div class="detail-value">Jl. Hewan Peliharaan No. 88, Jakarta</div>
            </div>
          </div>
          
          <div class="detail-row">
            <div class="detail-icon" style="background: #f97316;">
              <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="2">
                <path d="M22 16.92v3a2 2 0 01-2.18 2 19.79 19.79 0 01-8.63-3.07 19.5 19.5 0 01-6-6 19.79 19.79 0 01-3.07-8.67A2 2 0 014.11 2h3a2 2 0 012 1.72 12.84 12.84 0 00.7 2.81 2 2 0 01-.45 2.11L8.09 9.91a16 16 0 006 6l1.27-1.27a2 2 0 012.11-.45 12.84 12.84 0 002.81.7A2 2 0 0122 16.92z"/>
              </svg>
            </div>
            <div class="detail-text">
              <div class="detail-label">Phone</div>
              <div class="detail-value">0812-3456-7890</div>
            </div>
          </div>
          
          <div class="detail-row">
            <div class="detail-icon" style="background: #8b5cf6;">
              <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="2">
                <circle cx="12" cy="12" r="10"/>
                <polyline points="12 6 12 12 16 14"/>
              </svg>
            </div>
            <div class="detail-text">
              <div class="detail-label">Hours</div>
              <div class="detail-value">Mon - Sun: 09.00 - 21.00 WIB</div>
            </div>
          </div>
        </div>
        
        <button on:click={openWhatsApp} class="btn-contact-wa">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor">
            <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413Z"/>
          </svg>
          Chat on WhatsApp
        </button>
      </div>
      
      <div class="contact-map">
        <iframe 
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3966.5234567890!2d106.8223456!3d-6.1945678!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zNsKwMTEnNDAuNCJTIDEwNsKwNDknMjAuNCJF!5e0!3m2!1sen!2sid!4v1234567890"
          width="100%" 
          height="100%" 
          style="border:0;" 
          allowfullscreen="" 
          loading="lazy" 
          referrerpolicy="no-referrer-when-downgrade"
          title="Lokasi Paws Petshop">
        </iframe>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="footer">
    <div class="footer-content">
      <div class="footer-brand">
        <div class="logo">
          <div class="logo-circle">
            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
              <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm0 18c-4.41 0-8-3.59-8-8s3.59-8 8-8 8 3.59 8 8-3.59 8-8 8z"/>
              <circle cx="8.5" cy="10.5" r="1.5"/>
              <circle cx="15.5" cy="10.5" r="1.5"/>
              <path d="M8.5 14.5c1 1.5 2.5 2 3.5 2s2.5-.5 3.5-2"/>
            </svg>
          </div>
          <span class="logo-text">Paws</span>
        </div>
        <p class="footer-desc">Your trusted partner for premium pet care and products.</p>
      </div>
      <div class="footer-bottom">
        <p>&copy; 2024 Paws Petshop. All rights reserved.</p>
      </div>
    </div>
  </footer>

  <!-- Floating WhatsApp -->
  <button on:click={openWhatsApp} class="floating-whatsapp" aria-label="Chat WhatsApp">
    <svg width="28" height="28" viewBox="0 0 24 24" fill="currentColor">
      <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413Z"/>
    </svg>
  </button>
</main>

<style>
  @import './styles.css';
</style>
