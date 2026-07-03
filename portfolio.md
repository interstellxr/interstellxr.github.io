---
layout: default
title: Portfolio
permalink: /portfolio/
---

# Photography & Astrophotography

<p class="portfolio-intro">A curated selection of deep-sky targets and terrestrial landscapes. Click on any image to view exposure details, equipment configurations, and processing notes.</p>

<div class="portfolio-grid">
    <div class="portfolio-item" onclick="openLightbox(this)">
        <img src="/assets/photography/m31.jpg" alt="Andromeda Galaxy (M31)" class="grid-thumb">
        <div class="item-summary">
            <h3>Andromeda Galaxy (M31)</h3>
            <span class="category">Astrophotography</span>
        </div>
        <div class="hidden-details">
            <h2>Andromeda Galaxy (M31)</h2>
            <p class="photo-comment">This is one my first ever astrophotographs. I took it with my old Nikon D3400 mounted on a Skywatcher 200/1000 explorer telescope. At that focal length, I was too zoomed in and so this image is in fact a mosaic of three panels stitched together!</p>
            <table class="specs-table">
                <tr><td><strong>Target</strong></td><td>Messier 31</td></tr>
                <tr><td><strong>Integration</strong></td><td>I think around 8 hours total</td></tr>
                <tr><td><strong>Equipment</strong></td><td>Skywatcher 200/1000P, EQ6R-Pro</td></tr>
                <tr><td><strong>Camera</strong></td><td>Nikon D3400 (unmodified)</td></tr>
            </table>
        </div>
    </div>

    <div class="portfolio-item" onclick="openLightbox(this)">
        <img src="/assets/photography/m45.jpg" alt="The Pleiades (M45)" class="grid-thumb">
        <div class="item-summary">
            <h3>The Pleiades (M45)</h3>
            <span class="category">Astrophotography</span>
        </div>
        <div class="hidden-details">
            <h2>The Pleiades (M45)</h2>
            <p class="photo-comment">I think this might be my favorite astrophoto I've ever taken, as I really love the blue wisps of nebulae between the infamous seven sisters. Perhaps an easy target, but rewarding nonetheless!</p>
            <table class="specs-table">
                <tr><td><strong>Target</strong></td><td>Messier 45</td></tr>
                <tr><td><strong>Integration</strong></td><td>6 hours total exposure</td></tr>
                <tr><td><strong>Equipment</strong></td><td>Skywatcher 200/1000P, EQ6R-Pro</td></tr>
                <tr><td><strong>Camera</strong></td><td>ToupTek 26000 Color CMOS Camera</td></tr>
            </table>
        </div>
    </div>
</div>

<div id="portfolio-lightbox" class="lightbox" onclick="closeLightbox(event)">
    <div class="lightbox-content" onclick="event.stopPropagation()">
        <div class="image-viewer">
            <img id="lightbox-img" src="" alt="Expanded View">
        </div>
        <div id="lightbox-side-panel" class="side-panel">
            </div>
        <button class="close-btn" onclick="closeLightbox(event)">&times;</button>
    </div>
</div>

<script>
function openLightbox(element) {
    const thumbSrc = element.querySelector('.grid-thumb').src;
    const detailsHtml = element.querySelector('.hidden-details').innerHTML;
    
    document.getElementById('lightbox-img').src = thumbSrc;
    document.getElementById('lightbox-side-panel').innerHTML = detailsHtml;
    document.getElementById('portfolio-lightbox').classList.add('active');
    document.body.style.overflow = 'hidden'; // Lock background scrolling
}

function closeLightbox(event) {
    document.getElementById('portfolio-lightbox').classList.remove('active');
    document.body.style.overflow = ''; // Unlock background scrolling
}

// Close panel via keyboard Escape button
document.addEventListener('keydown', function(e) {
    if (e.key === 'Escape') closeLightbox();
});
</script>
