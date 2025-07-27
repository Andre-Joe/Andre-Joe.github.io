---
layout: default
title: Andre Joe Mhawej Portfolio
---

<div style="text-align: center; margin-top: 30px;">
  <a href="/" onclick="trackClick('Logo Click')">
    <img src="/assets/me.jpg" alt="Logo"
         style="height:120px; width:120px; border-radius:50%; object-fit:cover; box-shadow: 0 0 8px rgba(0,0,0,0.3);" />
  </a>
</div>

<h1 style="text-align: center; margin-top: 20px;">
  Future AI Engineer | Deep Learning & Computer Vision Enthusiast
</h1>

<p style="text-align: center;">
  Explore my journey in AI, certifications, and academic excellence.
</p>

---

## About Me

I'm Andre-Joe, a university student currently pursuing a degree in Artificial Intelligence at Arab Open University.  
I have one year left until graduation, and I’m especially interested in deep learning and computer vision.

---

## Certifications

For a complete list of my Coursera certifications, please visit my  
<a href="https://www.coursera.org/user/b2be56243c7bbe7e10eecb1fac05bd18" target="_blank" rel="noopener"
onclick="trackClick('Coursera Profile')">Coursera profile</a>.  

You can also view my  
<a href="https://freecodecamp.org/certification/Andre-Joe/machine-learning-with-python-v7" target="_blank" rel="noopener"
onclick="trackClick('FreeCodeCamp Certificate')">freeCodeCamp Machine Learning Certification</a>.

---

## Academic Transcript

I currently hold a GPA of **3.92/4.0** at Arab Open University.  
My full academic transcript is available <a href="/assets/transcript.pdf" onclick="trackClick('Transcript Click')">here</a>.

---

## Projects

### Cat-Dog CNN Classifier Project

A convolutional neural network built to classify images of cats and dogs.  
The passing accuracy for this task was 63%, and my model achieved 70%.  
This project was completed as part of my freeCodeCamp machine learning with python certification.

<div style="display: flex; flex-direction: column; gap: 15px; margin-bottom: 15px;">
  <img src="/assets/model.png" alt="Model Architecture" style="width: 60%; border-radius: 8px; box-shadow: 0 0 5px rgba(0,0,0,0.2);" />
  <img src="/assets/accuracy.png" alt="Model Accuracy" style="width: 60%; border-radius: 8px; box-shadow: 0 0 5px rgba(0,0,0,0.2);" />
</div>

<a href="https://colab.research.google.com/drive/1OQMpxaVBw8XNd-6eqcNwOxnmNrZa9W2J?usp=sharing" target="_blank" rel="noopener"
onclick="trackClick('Cat-Dog Colab')">Colab Notebook</a>

---

### Municipality Elections Data Science Project

Analyzed municipality election results to uncover voting patterns and trends using data visualization and statistical techniques.  
Disclaimer: The election data analyzed is based on pictures of final results sheets. The analysis is for educational purposes only.

<img src="/assets/stats.jpg" alt="Election Statistics" style="width: 60%; border-radius: 8px; box-shadow: 0 0 5px rgba(0,0,0,0.2);" />
  
<a href="https://colab.research.google.com/drive/1zdQZnuQ0uwVVV6xGbUQlaIkhDguMoZm_?usp=sharing" target="_blank" rel="noopener"
onclick="trackClick('Elections Colab')">Colab Notebook</a>

---

### Customer Churn Machine Learning Project

Built a baseline churn prediction model, then improved its performance through hyperparameter tuning with GridSearchCV.

<img src="/assets/comparison.png" alt="Churn Model Comparison" style="width: 60%; border-radius: 8px; margin-top: 10px; box-shadow: 0 0 5px rgba(0,0,0,0.2);" />

<a href="https://colab.research.google.com/drive/1DZbKLW_lr_extvUqsPHrAvZjkwLzxo83?usp=sharing" target="_blank" rel="noopener"
onclick="trackClick('Churn Colab')">Colab Notebook</a>

---

## Contact Me

- Email: <a href="mailto:amhawej38@gmail.com" style="text-decoration:none; color:inherit;"
onclick="trackClick('Email Click')">amhawej38@gmail.com</a>  
- Phone: <a href="tel:+96171679208" style="text-decoration:none; color:inherit;"
onclick="trackClick('Phone Click')">+961 71 679 208</a>

---

<script>
  function trackClick(label) {
    if (typeof gtag === 'function') {
      gtag('event', 'click', {
        event_category: 'link',
        event_label: label
      });
    }
  }

  document.querySelectorAll('a').forEach(link => {
    link.setAttribute('target', '_blank');
    link.setAttribute('rel', 'noopener');
  });
</script>
