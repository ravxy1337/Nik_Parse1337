# NIK Parse API

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=42&duration=3000&pause=1000&color=00D9FF&center=true&vCenter=true&width=600&lines=NIK+Parse+API;Indonesian+Identity+Parser;Lightning+Fast+%26+Accurate;Built+for+Developers" alt="NIK Parse API" />
  
  <br><br>
  
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=18&duration=2000&pause=500&color=FF6B6B&center=true&vCenter=true&width=500&lines=Parse+Indonesian+NIK+instantly;Extract+detailed+information;Secure+and+reliable+API;Ready+for+production+use" alt="Features" />
</div>

---

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Source+Code+Pro&size=24&duration=2500&pause=800&color=4ECDC4&center=true&vCenter=true&width=400&lines=FEATURES;AMAZING+FEATURES" alt="Features Header" />
</div>

<table align="center">
<tr>
<td align="center" width="50%">

<img src="https://readme-typing-svg.demolab.com?font=Roboto+Mono&size=16&duration=2000&pause=500&color=95E1D3&center=true&vCenter=true&width=300&lines=ULTRA+FAST;Millisecond+Response+Time" alt="Ultra Fast" />

Parse NIK dalam hitungan milliseconds dengan performa tinggi

</td>
<td align="center" width="50%">

<img src="https://readme-typing-svg.demolab.com?font=Roboto+Mono&size=16&duration=2000&pause=500&color=F38BA8&center=true&vCenter=true&width=300&lines=HIGHLY+ACCURATE;100%25+Precision+Rate" alt="Accurate" />

Validasi dan ekstraksi data yang sangat tepat dan terpercaya

</td>
</tr>
<tr>
<td align="center">

<img src="https://readme-typing-svg.demolab.com?font=Roboto+Mono&size=16&duration=2000&pause=500&color=A8DADC&center=true&vCenter=true&width=300&lines=ENTERPRISE+SECURE;Bank+Grade+Security" alt="Secure" />

API yang aman dengan enkripsi tingkat enterprise

</td>
<td align="center">

<img src="https://readme-typing-svg.demolab.com?font=Roboto+Mono&size=16&duration=2000&pause=500&color=FFD23F&center=true&vCenter=true&width=300&lines=EASY+INTEGRATION;One+Line+Implementation" alt="Easy" />

Simple REST API yang mudah diintegrasikan ke semua platform

</td>
</tr>
</table>

---

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Source+Code+Pro&size=28&duration=3000&pause=1000&color=FF6B9D&center=true&vCenter=true&width=500&lines=QUICK+START+GUIDE;GET+STARTED+NOW" alt="Quick Start" />
</div>

### Base URL
```
https://parse1337.vercel.app
```

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=20&duration=2500&pause=800&color=6C5CE7&center=true&vCenter=true&width=400&lines=API+ENDPOINTS;CHOOSE+YOUR+METHOD" alt="Endpoints" />
</div>

| Method | Endpoint | Description |
|--------|----------|-------------|
| **POST** | `/api/nik/parse` | Parse NIK menggunakan JSON payload |
| **GET** | `/api/nik/parse?nik=<number>` | Parse NIK menggunakan query parameter |

---

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Source+Code+Pro&size=26&duration=3000&pause=1000&color=00CEC9&center=true&vCenter=true&width=500&lines=CODE+EXAMPLES;IMPLEMENTATION+GUIDE" alt="Code Examples" />
</div>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=18&duration=2000&pause=500&color=FD79A8&center=true&vCenter=true&width=400&lines=JavaScript+Implementation;Modern+Async+Await" alt="JavaScript" />
</div>

```javascript
// Modern JavaScript dengan async/await
const parseNIK = async (nik) => {
  try {
    const response = await fetch('https://parse1337.vercel.app/api/nik/parse', {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json',
      },
      body: JSON.stringify({ nik: nik })
    });
    
    const result = await response.json();
    console.log(result);
    return result;
  } catch (error) {
    console.error('Error parsing NIK:', error);
    throw error;
  }
};

// Penggunaan
parseNIK('3201234567890001').then(result => {
  console.log('Parsed Data:', result.data);
});
```

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=18&duration=2000&pause=500&color=A29BFE&center=true&vCenter=true&width=400&lines=cURL+Commands;Terminal+Ready" alt="cURL" />
</div>

**POST Request**
```bash
curl -X POST https://parse1337.vercel.app/api/nik/parse \
  -H "Content-Type: application/json" \
  -H "User-Agent: NIK-Parser/1.0" \
  -d '{"nik": "3201234567890001"}'
```

**GET Request**
```bash
curl "https://parse1337.vercel.app/api/nik/parse?nik=3201234567890001" \
  -H "Accept: application/json"
```

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=18&duration=2000&pause=500&color=55A3FF&center=true&vCenter=true&width=400&lines=Python+Implementation;Data+Science+Ready" alt="Python" />
</div>

```python
import requests
import json
from typing import Dict, Any

class NIKParser:
    def __init__(self):
        self.base_url = "https://parse1337.vercel.app/api/nik/parse"
        self.session = requests.Session()
        self.session.headers.update({
            'Content-Type': 'application/json',
            'User-Agent': 'NIK-Parser-Python/1.0'
        })
    
    def parse(self, nik: str) -> Dict[str, Any]:
        """Parse Indonesian NIK and extract detailed information"""
        try:
            response = self.session.post(self.base_url, json={"nik": nik})
            response.raise_for_status()
            return response.json()
        except requests.RequestException as e:
            return {"status": "error", "message": f"Request failed: {e}"}

# Usage
parser = NIKParser()
result = parser.parse("3201234567890001")
print(json.dumps(result, indent=2, ensure_ascii=False))
```

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=18&duration=2000&pause=500&color=FF7675&center=true&vCenter=true&width=400&lines=React+Component;Modern+Frontend" alt="React" />
</div>

```jsx
import React, { useState, useCallback } from 'react';
import axios from 'axios';

const NIKParserComponent = () => {
  const [nik, setNik] = useState('');
  const [result, setResult] = useState(null);
  const [loading, setLoading] = useState(false);
  const [error, setError] = useState(null);

  const parseNIK = useCallback(async () => {
    if (!nik || nik.length !== 16) {
      setError('NIK harus 16 digit');
      return;
    }

    setLoading(true);
    setError(null);
    
    try {
      const response = await axios.post('https://parse1337.vercel.app/api/nik/parse', {
        nik: nik
      });
      
      setResult(response.data);
    } catch (err) {
      setError('Gagal memparse NIK');
    } finally {
      setLoading(false);
    }
  }, [nik]);

  return (
    <div className="nik-parser">
      <input 
        type="text"
        value={nik} 
        onChange={(e) => setNik(e.target.value.replace(/\D/g, '').slice(0, 16))}
        placeholder="Masukkan 16 digit NIK..."
        maxLength={16}
      />
      <button onClick={parseNIK} disabled={loading}>
        {loading ? 'Parsing...' : 'Parse NIK'}
      </button>
      
      {error && <div className="error">{error}</div>}
      {result && result.status === 'success' && (
        <div className="result">
          <h3>Data Berhasil Diparsing:</h3>
          <pre>{JSON.stringify(result.data, null, 2)}</pre>
        </div>
      )}
    </div>
  );
};

export default NIKParserComponent;
```

---

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Source+Code+Pro&size=26&duration=3000&pause=1000&color=E17055&center=true&vCenter=true&width=500&lines=RESPONSE+FORMAT;DATA+STRUCTURE" alt="Response Format" />
</div>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Roboto+Mono&size=16&duration=2000&pause=500&color=00B894&center=true&vCenter=true&width=300&lines=SUCCESS+RESPONSE;COMPLETE+DATA" alt="Success" />
</div>

```json
{
  "status": "success",
  "pesan": "NIK valid dan berhasil diparsing",
  "data": {
    "nik": "3201234567890001",
    "kelamin": "LAKI-LAKI",
    "lahir": "23/45/1990",
    "provinsi": "JAWA BARAT", 
    "kotakab": "KABUPATEN BOGOR",
    "kecamatan": "CIBINONG",
    "uniqcode": "0001",
    "tambahan": {
      "kodepos": "43271",
      "pasaran": "Senin Legi",
      "usia": "34 Tahun 2 Bulan 15 Hari",
      "ultah": "10 bulan 15 hari lagi",
      "zodiak": "Capricorn", 
      "tahunLahir": "1990",
      "tempatLahir": "JAWA BARAT"
    }
  }
}
```

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Roboto+Mono&size=16&duration=2000&pause=500&color=E84393&center=true&vCenter=true&width=300&lines=ERROR+RESPONSE;VALIDATION+INFO" alt="Error" />
</div>

```json
{
  "status": "error",
  "pesan": "NIK harus tepat 16 digit angka",
  "details": {
    "code": "INVALID_FORMAT",
    "received_length": 15,
    "expected_length": 16
  }
}
```

---

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Source+Code+Pro&size=26&duration=3000&pause=1000&color=FDCB6E&center=true&vCenter=true&width=500&lines=NIK+STRUCTURE;UNDERSTAND+THE+FORMAT" alt="NIK Format" />
</div>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=18&duration=2500&pause=800&color=6C5CE7&center=true&vCenter=true&width=600&lines=16+DIGIT+STRUCTURE;DECODE+EVERY+PART" alt="Structure" />
</div>

```
Format NIK: XX.XXXX.DDMMYY.XXXX
            │  │    │      │
            │  │    │      └─── Nomor urut (0001-9999)
            │  │    └────────── Tanggal lahir (DDMMYY)
            │  └─────────────── Kode wilayah kecamatan  
            └────────────────── Kode provinsi & kabupaten/kota
```

**Contoh NIK Valid:**
- `3201234567890001` → Jawa Barat, Kabupaten Bogor
- `1101234567890001` → Aceh, Kabupaten Simeulue  
- `7371234567890001` → Sulawesi Selatan, Kota Makassar

---

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Source+Code+Pro&size=26&duration=3000&pause=1000&color=00CEC9&center=true&vCenter=true&width=500&lines=ADVANCED+USAGE;PRODUCTION+READY" alt="Advanced Usage" />
</div>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=18&duration=2000&pause=500&color=A29BFE&center=true&vCenter=true&width=400&lines=Node.js+Backend;Express+Integration" alt="Node.js" />
</div>

```javascript
const express = require('express');
const axios = require('axios');
const rateLimit = require('express-rate-limit');

const app = express();
app.use(express.json());

// Rate limiting
const limiter = rateLimit({
  windowMs: 15 * 60 * 1000, // 15 minutes
  max: 100 // limit each IP to 100 requests per windowMs
});

app.use('/api/nik', limiter);

// NIK validation middleware
const validateNIK = (req, res, next) => {
  const { nik } = req.body;
  
  if (!nik || !/^\d{16}$/.test(nik)) {
    return res.status(400).json({
      error: 'Invalid NIK format',
      message: 'NIK must be exactly 16 digits'
    });
  }
  
  next();
};

app.post('/api/nik/validate', validateNIK, async (req, res) => {
  try {
    const { nik } = req.body;
    
    const response = await axios.post('https://parse1337.vercel.app/api/nik/parse', {
      nik: nik
    }, {
      timeout: 5000,
      headers: {
        'Content-Type': 'application/json',
        'User-Agent': 'NIK-Validator-Service/1.0'
      }
    });
    
    // Add additional processing if needed
    const processedData = {
      ...response.data,
      timestamp: new Date().toISOString(),
      source: 'NIK-Parse-API'
    };
    
    res.json(processedData);
  } catch (error) {
    console.error('NIK validation error:', error.message);
    res.status(500).json({
      error: 'Validation service unavailable',
      message: 'Please try again later'
    });
  }
});

const PORT = process.env.PORT || 3000;
app.listen(PORT, () => {
  console.log(`NIK Validation Service running on port ${PORT}`);
});
```

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=18&duration=2000&pause=500&color=FF7675&center=true&vCenter=true&width=400&lines=React+Native;Mobile+Development" alt="React Native" />
</div>

```javascript
import React, { useState } from 'react';
import { View, Text, TextInput, TouchableOpacity, Alert } from 'react-native';

const NIKParser = () => {
  const [nik, setNik] = useState('');
  const [result, setResult] = useState(null);
  const [loading, setLoading] = useState(false);

  const parseNIK = async () => {
    if (!nik || nik.length !== 16) {
      Alert.alert('Error', 'NIK harus 16 digit');
      return;
    }

    setLoading(true);
    
    try {
      const response = await fetch('https://parse1337.vercel.app/api/nik/parse', {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json',
        },
        body: JSON.stringify({ nik }),
      });

      const data = await response.json();
      
      if (data.status === 'success') {
        setResult(data.data);
        Alert.alert('Berhasil', 'NIK berhasil diparsing!');
      } else {
        Alert.alert('Error', data.pesan);
      }
    } catch (error) {
      Alert.alert('Error', 'Gagal terhubung ke server');
    } finally {
      setLoading(false);
    }
  };

  return (
    <View style={{ padding: 20 }}>
      <Text style={{ fontSize: 24, fontWeight: 'bold', marginBottom: 20 }}>
        NIK Parser
      </Text>
      
      <TextInput
        style={{
          borderWidth: 1,
          borderColor: '#ddd',
          padding: 10,
          fontSize: 16,
          marginBottom: 20
        }}
        placeholder="Masukkan 16 digit NIK"
        value={nik}
        onChangeText={(text) => setNik(text.replace(/\D/g, '').slice(0, 16))}
        keyboardType="numeric"
        maxLength={16}
      />
      
      <TouchableOpacity
        style={{
          backgroundColor: loading ? '#ccc' : '#007AFF',
          padding: 15,
          borderRadius: 8,
          alignItems: 'center'
        }}
        onPress={parseNIK}
        disabled={loading}
      >
        <Text style={{ color: 'white', fontSize: 16, fontWeight: 'bold' }}>
          {loading ? 'Memproses...' : 'Parse NIK'}
        </Text>
      </TouchableOpacity>

      {result && (
        <View style={{ marginTop: 20 }}>
          <Text style={{ fontSize: 18, fontWeight: 'bold' }}>Hasil:</Text>
          <Text>Provinsi: {result.provinsi}</Text>
          <Text>Kab/Kota: {result.kotakab}</Text>
          <Text>Kecamatan: {result.kecamatan}</Text>
          <Text>Kelamin: {result.kelamin}</Text>
          <Text>Tanggal Lahir: {result.lahir}</Text>
        </View>
      )}
    </View>
  );
};

export default NIKParser;
```

---

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Source+Code+Pro&size=26&duration=3000&pause=1000&color=E84393&center=true&vCenter=true&width=500&lines=ERROR+HANDLING;ROBUST+VALIDATION" alt="Error Handling" />
</div>

| Status Code | Error Message | Description | Solution |
|-------------|---------------|-------------|----------|
| **400** | NIK harus 16 digit | Format NIK tidak sesuai | Pastikan NIK tepat 16 digit |
| **400** | NIK mengandung karakter non-digit | NIK harus angka semua | Gunakan hanya angka 0-9 |
| **400** | NIK tidak valid | NIK tidak dapat diparsing | Periksa kode wilayah NIK |
| **429** | Too many requests | Rate limit terlampaui | Tunggu beberapa saat sebelum request lagi |
| **500** | Internal server error | Kesalahan server | Coba lagi atau hubungi support |

---

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Source+Code+Pro&size=26&duration=3000&pause=1000&color=00B894&center=true&vCenter=true&width=500&lines=SECURITY+%26+PRIVACY;ENTERPRISE+GRADE" alt="Security" />
</div>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=16&duration=2000&pause=500&color=55A3FF&center=true&vCenter=true&width=500&lines=ZERO+DATA+RETENTION;STATELESS+PROCESSING;HTTPS+ENCRYPTION;NO+LOGGING" alt="Security Features" />
</div>

**Keamanan Data:**
- **Zero Logging** - Tidak ada data NIK yang disimpan atau dicatat
- **Stateless API** - Setiap request diproses independen tanpa menyimpan state
- **HTTPS Only** - Semua komunikasi menggunakan enkripsi SSL/TLS
- **No Personal Data Storage** - API tidak menyimpan informasi personal apapun
- **Rate Limiting** - Perlindungan terhadap abuse dan spam

**Privacy Policy:**
- Data NIK hanya diproses untuk parsing dan langsung dibuang
- Tidak ada tracking atau analytics pada data personal
- API tidak terhubung dengan database penyimpanan NIK
- Tidak ada sharing data dengan pihak ketiga

---

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Source+Code+Pro&size=26&duration=3000&pause=1000&color=FDCB6E&center=true&vCenter=true&width=500&lines=PERFORMANCE+%26+LIMITS;OPTIMIZE+YOUR+USAGE" alt="Performance" />
</div>

**Rate Limits:**
- **100 requests per minute** per IP address
- **1000 requests per hour** per IP address
- **10,000 requests per day** per IP address

**Response Times:**
- **Average:** < 100ms
- **95th percentile:** < 200ms
- **99th percentile:** < 500ms

**Best Practices:**
- Implement client-side caching untuk mengurangi duplicate requests
- Gunakan exponential backoff untuk retry logic
- Validasi NIK format di client sebelum mengirim ke API
- Batch multiple NIK jika memungkinkan

---

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Source+Code+Pro&size=26&duration=3000&pause=1000&color=A29BFE&center=true&vCenter=true&width=500&lines=CONTRIBUTING;OPEN+SOURCE+COMMUNITY" alt="Contributing" />
</div>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=16&duration=2000&pause=500&color=FF6B9D&center=true&vCenter=true&width=400&lines=WE+WELCOME+CONTRIBUTORS;JOIN+THE+COMMUNITY" alt="Welcome Contributors" />
</div>

Kontribusi sangat diterima! Berikut cara untuk berkontribusi:

**Development Setup:**
```bash
# Clone repository
git clone https://github.com/yourusername/nik-parse-api.git
cd nik-parse-api

# Install dependencies
npm install

# Setup environment variables
cp .env.example .env

# Run development server
npm run dev

# Run tests
npm test

# Run linting
npm run lint
```

**Contribution Guidelines:**
- Fork repository dan buat branch baru untuk fitur/bugfix
- Pastikan semua tests passing sebelum submit PR
- Ikuti coding standards yang sudah ada
- Update dokumentasi jika diperlukan
- Tambahkan tests untuk fitur baru

---

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Source+Code+Pro&size=26&duration=3000&pause=1000&color=FF7675&center=true&vCenter=true&width=500&lines=LICENSE+%26+CREDITS;OPEN+SOURCE+FOREVER" alt="License" />
</div>

**MIT License**

Copyright (c) 2025 NIK Parse API

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files, to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software.

**Acknowledgments:**
- Indonesian Government untuk spesifikasi format NIK
- Open Source Community untuk inspirasi dan dukungan
- Vercel untuk platform hosting yang reliable
- All contributors yang telah membantu pengembangan

---

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Source+Code+Pro&size=28&duration=4000&pause=1000&color=00D9FF&center=true&vCenter=true&width=600&lines=CONTACT+%26+SUPPORT;WE%27RE+HERE+TO+HELP" alt="Contact" />
</div>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=16&duration=2500&pause=800&color=6C5CE7&center=true&vCenter=true&width=500&lines=GitHub+Issues+for+bugs;GitHub+Discussions+for+questions;Email+for+business+inquiry" alt="Contact Methods" />
</div>

**Get Help:**
- **Bug Reports:** [GitHub Issues](https://github.com/yourusername/nik-parse-api/issues)
- **Feature Requests:** [GitHub Discussions](https://github.com/yourusername/nik-parse-api/discussions)
- **General Questions:** [GitHub Discussions Q&A](https://github.com/yourusername/nik-parse-api/discussions/categories/q-a)
- **Business Inquiry:** your.email@example.com

**Response Time:**
- Issues dan bug reports: **< 24 hours**
- Feature requests: **< 48 hours**  
- Business inquiries: **< 72 hours**

---

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=28&duration=3500&pause=1200&color=FF6B6B&center=true&vCenter=true&width=800&lines=Parsing+Indonesian+identity+with+precision;Building+bridges+between+data+and+developers;Code+that+connects%2C+APIs+that+empower;Innovation+through+intelligent+data+processing" alt="Mission Statement" />
</div>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=20&duration=4000&pause=1500&color=00D9FF&center=true&vCenter=true&width=700&lines=🚀+Lightning+fast+NIK+parsing;🎯+Accurate+data+extraction;🔒+Zero+data+retention+policy;🌟+Made+with+love+in+Indonesia" alt="Features Footer" />
</div>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Source+Code+Pro&size=16&duration=3000&pause=800&color=95E1D3&center=true&vCenter=true&width=600&lines=Thank+you+for+choosing+NIK+Parse+API;Star+⭐+this+repo+to+show+support;Follow+for+more+awesome+projects;Happy+coding%2C+Indonesian+developers!" alt="Gratitude" />
</div>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Roboto+Mono&size=14&duration=5000&pause=2000&color=A8DADC&center=true&vCenter=true&width=500&lines=©+2025+NIK+Parse+API;Open+source+•+MIT+Licensed;Crafted+with+passion+•+Powered+by+Vercel" alt="Copyright" />
</div>
