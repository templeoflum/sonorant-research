# **Uniform Data Standard (UDS) v1.1 — Loudspeaker Companies & Cabinets**

**UDS Version:** 1.1 (updated 2025-02-05)
**Changelog:** Removed modularity_transport criterion; updated weights to 5-criterion system; removed architecture-specific R&D flags.

Goal: collect comparable, source-grounded data on every company's speaker/cabinet designs, design philosophy, and case studies to fuel unorthodox, high-fidelity system design for 100–200 cap communal events.

---

## **0\) Global rules**

* Sources first: prefer manufacturer datasheets/whitepapers â†’ patents â†’ trusted press â†’ 3rd-party measurements. Capture URL \+ date for each fact.

* Measured vs. claimed: every spec has provenance: manufacturer|independent|derived and confidence: high|med|low.

* Units/normalization: SI; frequency in Hz; SPL in dB re 20 ÂµPa; sensitivity at 2.83 V/1 m (also store 1 W/1 m if supplied); power as AES/IEC if stated; angles in degrees (HxV).

* Nulls & estimates: use null for unknown, not â€œN/Aâ€. Derived values flagged provenance: derived with method.

* Taxonomy: tag designs using the UDS Tech Vocabulary (Section 6\) so cross-brand comparisons are queryable.

---

## **1\) Company record (one per brand)**

{  
  "company\_id": "alcons\_audio",  
  "name": "Alcons Audio",  
  "aka": \[\],  
  "founded\_year": null,  
  "hq\_country": "",  
  "key\_people": \[{"name":"","role":"","years":""}\],  
  "ownership": "private|public|division\_of:\<parent\>",  
  "lineage": {"predecessors": \[\], "spin\_offs": \[\]},  
  "philosophy": {  
    "tags": \["controlled\_directivity","low\_distortion","time\_alignment"\],  
    "summary": "2â€“5 sentence technical synopsis grounded in sources",  
    "notable\_quotes": \[{"quote":"","person":"","year":"","source":""}\]  
  },  
  "supply\_chain": {  
    "drivers\_in\_house": false,  
    "driver\_vendors": \["B\&C","BMS","PD","Faital","Eminence","SB Audience","Volt","Radian","ScanSpeak","Seas","Morel"\],  
    "amp\_dsp\_partners": \["Powersoft","Lake","Hypex","ICEpower","Trinnov","Dirac","miniDSP"\]  
  },  
  "standards\_cert": \["THX","EN54-24","IECEx","ATEX","Dolby\_Layout\_Ready","AES67","Dante"\],  
  "sources": \[\],  
  "audit\_notes": ""  
}

---

## **2\) Model record (one per loudspeaker/cabinet)**

{  
  "model\_id": "brand\_series\_model\_rev",  
  "company\_id": "alcons\_audio",  
  "name": "CRMS MkII",  
  "release\_year": null,  
  "status": "current|discontinued|prototype",  
  "application": \["touring","theatre","cinema","home","studio","industrial"\],  
  "form\_factor": "point\_source|line\_array|column|horn|open\_baffle|omni|sub|kick|coax\_monitor|main\_monitor",  
  "topology": {  
    "radiators": \["compression\_1.4in","cone\_12","cone\_15","AMT","planar","pro\_ribbon","coax\_cd"\],  
    "hf\_loading": \["os\_cd\_horn","diffraction\_slot","acoustic\_lens","multi\_entry\_horn"\],  
    "mf\_loading": \["sealed\_mid","cardioid\_mid","mid\_horn"\],  
    "lf\_alignment": \["sealed","reflex","passive\_radiator","bandpass\_4th","bandpass\_6th","ppsl","tapped\_horn","tl","paraflex","roar","front\_loaded\_horn","rear\_loaded\_horn","ripole"\],  
    "directivity\_methods": \["constant\_q\_horn","cardioid\_enclosure","gradient\_array","cbt\_column","steerable\_dsp","dipole","omni"\],  
    "ports": \["flared\_round","laminar\_slot","multi\_port","aperiodic\_resistive","variable\_length"\],  
    "structure": \["birch","marine\_ply","mdf\_selective","aluminum","composite","cld\_braced","3d\_printed\_waveguide"\]  
  },  
  "drivers": \[  
    {"position":"HF","make":"","model":"","exit\_mm":35.6,"material":"Be|Ti|Polyimide|Ribbon|ProRibbon"},  
    {"position":"MF","make":"","model":"","size\_in":10},  
    {"position":"LF","make":"","model":"","size\_in":15,"count":2,"arrangement":"ppsl|iso|front"}  
  \],  
  "key\_specs": {  
    "bandwidth\_hz": \[null,null\],  
    "f3\_hz": null,  
    "f10\_hz": null,  
    "sensitivity\_db\_2v83": null,  
    "sensitivity\_db\_1w": null,  
    "max\_spl\_db\_cont": null,  
    "max\_spl\_db\_peak": null,  
    "power\_handling\_w": {"aes": null, "program": null, "peak": null},  
    "impedance\_ohm\_nom": null,  
    "impedance\_ohm\_min": null,  
    "directivity\_nominal": "90x40",  
    "directivity\_map": \[{"freq\_hz":1000,"h\_deg":90,"v\_deg":40}\],  
    "di\_avg\_db\_500\_10k": null,  
    "thd\_percent\_at\_ref": {"freq\_hz":1000,"spl\_db":96,"value": null},  
    "group\_delay\_ms": \[{"freq\_hz":40,"ms":null},{"freq\_hz":80,"ms":null}\],  
    "dimensions\_mm": {"w":null,"h":null,"d":null},  
    "weight\_kg": null  
  },  
  "integration": {  
    "xover\_points\_hz": \[null,null\],  
    "recommended\_processing": "FIR/IIR notes; cardioid filters",  
    "amp\_requirements": {"ways":2,"per\_way\_w": \[null,null\],"min\_headroom\_db":6},  
    "connections": "NL4/NL8/plate\_amp",  
    "mounting": \["pole","stack","fly\_points","array\_hardware"\]  
  },  
  "variants": \[{"name":"","differs\_by":"coverage|finish|impedance|amp\_dsp"}\],  
  "measurements": {  
    "polars\_available": true,  
    "cea2010\_sub": \[{"freq\_hz":31.5,"db":null}\],  
    "waterfall\_etc": false,  
    "source\_links": \[\]  
  },  
  "case\_studies": \[  
    {  
      "site":"Club/Theatre/Cinema name",  
      "type":"club|theatre|cinema|outdoor",  
      "capacity": 180,  
      "geometry":"WxDxH m",  
      "deployment":"L/R \+ fills \+ subs",  
      "outcomes":"short bullet points (e.g., pattern control, SPL headroom)",  
      "lessons":"transferable design insights",  
      "sources":\[\]  
    }  
  \],  
  "criticisms\_limits": \["size for crossover target","port turbulence at 120 dB"\],  
  "ip\_patents": \[{"id":"","year":null,"title":"","relevance":"horn|port|array|cardioid"}\],  
  "r\_and\_d\_flags": \["psychoacoustic\_potential","infra\_ready","cardioid\_capable","temporal\_correction","passive\_directivity","coaxial\_coherent","ob\_hybrid\_candidate"\],  
  "provenance": \[{"field":"key\_specs.max\_spl\_db\_peak","source":"","provenance":"manufacturer","confidence":"med"}\],  
  "last\_audited": "YYYY-MM-DD"  
}

---

## **3\) Case-study record (reusable across models)**

{  
  "case\_id": "venue\_yyyy\_brand\_model",  
  "venue": {"name":"","city":"","country":""},  
  "type": "club|theatre|cinema|festival|house\_of\_worship|industrial",  
  "capacity": null,  
  "room\_dims\_m": {"w":null,"d":null,"h":null},  
  "system\_layout": {"mains":"L/R|LCR|array","fills":"front|out|delay","subs":"infra+kicks|cardioid"},  
  "coverage\_target\_deg": "HxV per zone",  
  "outcomes": \["SPL @ FOH","complaints reduced","mix translation"\],  
  "measured\_data": {"spl\_dBA\_slow":null,"spl\_dBC\_fast":null,"polars\_collected":false},  
  "lessons": \["what to steal"\],  
  "sources": \[\]  
}

---

## **4\) Derived metrics (standard methods)**

* Max SPL (approx.) if not provided:

   spl\_max\_est\_db \= sensitivity\_db\_2v83 \+ 10\*log10(P\_cont\_w) \+ crest\_db

   Store method:"derived", crest\_db used (e.g., 3 dB for program, 6 dB for short peak).

* DI average: average DI over 500 Hzâ€“10 kHz from polar map or manufacturer DI plot; store window.

* LF extension: compute F3/F10 by interpolation from magnitude data; store points and method.

* Group delay checkpoints: store at 40, 60, 80, 100 Hz for subs/kicks; at crossover for tops.

---

## **5\) R\&D relevance scoring (per model; weights fixed)**

{
  "scores": {
    "hf_clarity_transient": 0.0,
    "directivity_control_imaging": 0.0,
    "sub_weight_infrasonic": 0.0,
    "psychoacoustic_potential": 0.0,
    "small_room_viability": 0.0
  },
  "weights": {
    "hf_clarity_transient": 0.23,
    "directivity_control_imaging": 0.23,
    "sub_weight_infrasonic": 0.23,
    "psychoacoustic_potential": 0.20,
    "small_room_viability": 0.11
  },
  "composite": 0.00,
  "rationale": {
    "hf_clarity_transient": "driver/waveguide clarity, transient response, HD data",
    "directivity_control_imaging": "pattern control, imaging stability, beam steering capability",
    "sub_weight_infrasonic": "LF extension, efficiency-to-weight ratio, infrasonic capability",
    "psychoacoustic_potential": "immersion, spatial perception, soundstage depth",
    "small_room_viability": "suitability for 100-200 cap venues, cardioid/dipole/low group delay"
  }
}

---

## **6\) UDS Tech Vocabulary (controlled tags)**

* Radiators: compression\_1in|1\_4in|2in|ring\_radiator|coax\_cd|cone|AMT|ribbon|planar|electrostatic|bmr|dml|pro\_ribbon|piezo|ionic\_plasma

* HF loading: os\_cd\_horn|exp\_horn|tractrix|lecleach|diffraction\_slot|acoustic\_lens|multicell|paraline|multi\_entry\_horn|waveguide\_large

* MF loading: sealed\_mid|cardioid\_mid|mid\_horn|coax\_mid\_hf

* LF alignment: sealed|reflex|passive\_radiator|bandpass\_4th|bandpass\_6th|bandpass\_8th|ppsl|isobaric|tapped\_horn|tl|mltl|paraflex|roar|front\_loaded\_horn|rear\_loaded\_horn|ripole|manifold

* Directivity: constant\_q\_horn|cardioid\_enclosure|gradient\_array|end\_fire|cbt\_column|steerable\_dsp|dipole|omni|point\_source\_coherent

* Ports: flared\_round|laminar\_slot|multi\_port|aperiodic\_resistive|variable\_length

* Structure: birch|marine\_ply|mdf\_selective|aluminum|steel|composite|cld\_braced|honeycomb|3d\_printed\_waveguide

* Integration: passive\_xover|active\_plate\_amp|external\_amp\_dsp|fir\_linear\_phase|all\_pass\_alignment|cardioid\_filters

* R\&D flags: infra\_ready|cardioid\_capable|psychoacoustic\_potential|temporal\_correction|passive\_directivity|coaxial\_coherent|ob\_hybrid\_candidate

---

## **7\) CSV extracts (for fast filtering)**

companies.csv

company\_id,name,founded\_year,hq\_country,ownership,philosophy\_tags,drivers\_in\_house,amp\_dsp\_partners,standards\_cert,last\_audited

models.csv

model\_id,company\_id,name,status,application,form\_factor,radiators,hf\_loading,lf\_alignment,directivity\_methods,bandwidth\_low,bandwidth\_high,f3,f10,sens\_2v83,max\_spl\_peak,directivity\_nominal,di\_avg\_500\_10k,weight\_kg,w\_mm,h\_mm,d\_mm,last\_audited

cases.csv

case\_id,model\_id,venue,type,capacity,room\_w,room\_d,room\_h,layout,subs\_mode,measured\_A,measured\_C,outcomes,lessons,sources

---

## **8\) Source record (attach anywhere)**

{"title":"","url":"","publisher":"","date":"","type":"datasheet|whitepaper|press|review|measurement|patent","notes":"","confidence":"high|med|low"}

---

## **9\) QA checklist (per model)**

* All required fields present; units normalized; provenance/confidence set.

* Tech tags from Section 6 applied (â‰¥1 in each applicable domain).

* At least 5 sources or an audit note explaining scarcity.

* Measured vs claimed clearly separated.

* Derived metrics flagged with method.

* Last-audited date set.

---

## **10\) File conventions**

* Markdown dossier: reports/\<category\>/\<company\>/\<model\>.md

* JSON sidecar: reports/\<category\>/\<company\>/\<model\>.json

* Indexes in reports/\_indexes/\*.csv

---

## **11\) Minimal dossier template (Markdown)**

\# \<Model\> â€” \<Company\>

Use: \<application\> â€¢ Form factor: \<form\_factor\> â€¢ Status: \<status\>    
Topology: \<radiators \+ loading \+ LF alignment \+ directivity\>    
Key specs: \<bandwidth / F3 / sens @2.83V / max SPL / nominal pattern / weight\>    
Design notes: \<2â€“4 bullets grounded in sources\>    
Case studies: \<venue, year, takeaway\>    
Criticisms/limits: \<bullets\>    
R\&D flags: \<list\>    
Sources: \[1\] â€¦ \[2\] â€¦    
Audit notes: \<gaps, conflicts\>

---

## **12\) Ingestion protocol (agent)**

1. Resolve company\_id; crawl official site for product index.

2. Create one Model record per cabinet version (include variants).

3. Parse PDFs for specs; extract polars/DI where available.

4. Search patents with \<company\> \+ loudspeaker | horn | port | array | cardioid.

5. Gather case studies from integrators/venues; attach lessons.

6. Populate tech tags; compute derived metrics; score R\&D relevance.

7. Validate with QA checklist; write Markdown \+ JSON \+ CSV rows.

