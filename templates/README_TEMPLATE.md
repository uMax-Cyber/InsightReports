# Report Template (copy this)

Use this structure for your reports. Replace ALL_CAPS placeholders.

## Required sections:
1. Title + date + context
2. "If short — three phrases" (verdict block)
3. Stat cards (4-6 key metrics)
4. For each problem: description → SVG animation → fix section → SVG animation (after)
5. Summary table
6. Action plan (numbered, with time estimates)
7. Footer: methodology note + data sources

## SVG Animation Pattern:
```html
<svg width="600" height="300" style="background:#0d1117;border-radius:12px">
  <!-- Animated element -->
  <rect rx="10" fill="#f85149" width="90" height="24">
    <animate attributeName="x" values="140;400" dur="1.5s" repeatCount="indefinite"/>
  </rect>
  <!-- Staggered grid -->
  <g transform="translate(100,200)">
    <rect x="0" y="0" width="18" height="18" fill="#f85149">
      <animate attributeName="opacity" values="0;1" dur="0.3s" begin="0s" fill="freeze"/>
    </rect>
    <!-- more rects with begin="0.03s", "0.06s"... for stagger -->
  </g>
</svg>
```
