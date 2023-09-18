### Education

### Work Experience

Research Scientist
- xyz
- 
Apisero
-
-

Accenture
- xyz
- 

### Projects

<ul class="timeline timeline-split">
    {% for period in site.periods %}
      {% if period.name %}
        <li class="timeline-item period">
          <div class="timeline-info"></div>
          <div class="timeline-marker"></div>
          <div class="timeline-content">
            <h2 class="timeline-title">{{ period.name }}</h2>
          </div>
        </li>
      {% endif %}
      {% for event_hash in period.events %}
        {% for event in event_hash %}
        <li class="timeline-item">
          <div class="timeline-info">
            <span>{{ event[0] }}</span>
          </div>
          <div class="timeline-marker"></div>
          <div class="timeline-content">
            <h3 class="timeline-title">{{ event[1] }}</h3>
          </div>
        </li>
        {% endfor %}
      {% endfor %}
    {% endfor %}

    {% if site.show_today %}
      <li class="timeline-item inactive">
        <div class="timeline-info">
          <span>Today</span>
        </div>
        <div class="timeline-marker"></div>
        <div class="timeline-content">
          <h3 class="timeline-title">&nbsp;</h3>
        </div>
      </li>
    {% endif %}
  </ul>
