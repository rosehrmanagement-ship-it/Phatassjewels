   SCROLL REVEAL
   =============================================================== */
function observeReveal() {
  const io = new IntersectionObserver(entries => {
    entries.forEach(en => {
      if (en.isIntersecting) {
        en.target.classList.add('in');
        io.unobserve(en.target);
      }
    });
  }, { threshold: 0.12, rootMargin: '0px 0px -50px 0px' });
  document.querySelectorAll('.reveal').forEach(el => io.observe(el));
}

/* ===============================================================
   INIT
   =============================================================== */
document.getElementById('year').textContent = new Date().getFullYear();
renderProducts();
renderCart();
</script>

</body>
</html>
