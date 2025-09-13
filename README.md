<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Orbitron&weight=900&size=45&duration=3000&pause=1000&color=00D4FF&center=true&vCenter=true&width=700&lines=NIK+Parse+API;Parser+Identitas+Indonesia;Cepat+%26+Akurat;Siap+untuk+Produksi" alt="NIK Parse API" />
  
  <br><br>
  
  <img src="https://readme-typing-svg.demolab.com?font=Exo+2&weight=600&size=20&duration=2500&pause=800&color=FF3366&center=true&vCenter=true&width=600&lines=Parse+NIK+Indonesia+secara+instan;Ekstrak+informasi+detail+lengkap;API+yang+aman+dan+terpercaya;Siap+digunakan+untuk+produksi" alt="Features" />
</div>

---

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Rajdhani&weight=700&size=28&duration=2800&pause=900&color=00FF88&center=true&vCenter=true&width=500&lines=FITUR+UNGGULAN;KENAPA+PILIH+KAMI" alt="Features Header" />
</div>

<table align="center">
<tr>
<td align="center" width="50%">

<img src="https://readme-typing-svg.demolab.com?font=Space+Mono&weight=700&size=18&duration=2200&pause=600&color=FFD700&center=true&vCenter=true&width=350&lines=SUPER+CEPAT;Respon+dalam+Milidetik" alt="Ultra Fast" />

Parse NIK dalam hitungan milidetik dengan performa tinggi yang konsisten

</td>
<td align="center" width="50%">

<img src="https://readme-typing-svg.demolab.com?font=Space+Mono&weight=700&size=18&duration=2200&pause=600&color=FF6B9D&center=true&vCenter=true&width=350&lines=AKURASI+TINGGI;Presisi+100%25" alt="Accurate" />

Validasi dan ekstraksi data yang sangat tepat dengan tingkat akurasi maksimal

</td>
</tr>
<tr>
<td align="center">

<img src="https://readme-typing-svg.demolab.com?font=Space+Mono&weight=700&size=18&duration=2200&pause=600&color=00E5FF&center=true&vCenter=true&width=350&lines=KEAMANAN+TINGGI;Enkripsi+Enterprise" alt="Secure" />

API yang aman dengan standar keamanan tingkat enterprise untuk data sensitif

</td>
<td align="center">

<img src="https://readme-typing-svg.demolab.com?font=Space+Mono&weight=700&size=18&duration=2200&pause=600&color=FF9F43&center=true&vCenter=true&width=350&lines=MUDAH+INTEGRASI;Satu+Baris+Kode" alt="Easy" />

REST API sederhana yang mudah diintegrasikan ke semua platform dan framework

</td>
</tr>
</table>

---

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Rajdhani&weight=700&size=30&duration=3200&pause=1100&color=A855F7&center=true&vCenter=true&width=600&lines=PANDUAN+CEPAT;MULAI+SEKARANG+JUGA" alt="Quick Start" />
</div>

### Base URL
```
https://parse1337.vercel.app
```

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Orbitron&weight=600&size=22&duration=2600&pause=850&color=10B981&center=true&vCenter=true&width=450&lines=ENDPOINT+API;PILIH+METODE+ANDA" alt="Endpoints" />
</div>

| Metode | Endpoint | Deskripsi |
|--------|----------|-----------|
| **POST** | `/api/nik/parse` | Parse NIK menggunakan JSON payload |
| **GET** | `/api/nik/parse?nik=<nomor>` | Parse NIK menggunakan query parameter |

---

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Rajdhani&weight=700&size=28&duration=3400&pause=1200&color=EF4444&center=true&vCenter=true&width=550&lines=CONTOH+KODE;PANDUAN+IMPLEMENTASI" alt="Code Examples" />
</div>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Exo+2&weight=600&size=20&duration=2400&pause=700&color=8B5CF6&center=true&vCenter=true&width=450&lines=Implementasi+JavaScript;Async+Await+Modern" alt="JavaScript" />
</div>

```javascript
// JavaScript modern dengan async/await
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

// Cara penggunaan
parseNIK('3201234567890001').then(result => {
  console.log('Data yang diparsing:', result.data);
});
```

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Exo+2&weight=600&size=20&duration=2400&pause=700&color=06B6D4&center=true&vCenter=true&width=450&lines=Perintah+cURL;Siap+untuk+Terminal" alt="cURL" />
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
  <img src="https://readme-typing-svg.demolab.com?font=Exo+2&weight=600&size=20&duration=2400&pause=700&color=F59E0B&center=true&vCenter=true&width=450&lines=Implementasi+Python;Data+Science+Ready" alt="Python" />
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
        """Parse NIK Indonesia dan ekstrak informasi detail"""
        try:
            response = self.session.post(self.base_url, json={"nik": nik})
            response.raise_for_status()
            return response.json()
        except requests.RequestException as e:
            return {"status": "error", "message": f"Request gagal: {e}"}

# Cara penggunaan
parser = NIKParser()
result = parser.parse("3201234567890001")
print(json.dumps(result, indent=2, ensure_ascii=False))
```

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Exo+2&weight=600&size=20&duration=2400&pause=700&color=EC4899&center=true&vCenter=true&width=450&lines=Komponen+React;Frontend+Modern" alt="React" />
</div>

```jsx
import React, { useState, useCallback } from 'react';
import axios from 'axios';

const KomponenParserNIK = () => {
  const [nik, setNik] = useState('');
  const [hasil, setHasil] = useState(null);
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
      
      setHasil(response.data);
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
        {loading ? 'Memproses...' : 'Parse NIK'}
      </button>
      
      {error && <div className="error">{error}</div>}
      {hasil && hasil.status === 'success' && (
        <div className="result">
          <h3>Data Berhasil Diparsing:</h3>
          <pre>{JSON.stringify(hasil.data, null, 2)}</pre>
        </div>
      )}
    </div>
  );
};

export default KomponenParserNIK;
```

---

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Rajdhani&weight=700&size=28&duration=3600&pause=1300&color=059669&center=true&vCenter=true&width=550&lines=FORMAT+RESPONS;STRUKTUR+DATA" alt="Response Format" />
</div>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Space+Mono&weight=700&size=18&duration=2400&pause=600&color=22C55E&center=true&vCenter=true&width=350&lines=RESPONS+BERHASIL;DATA+LENGKAP" alt="Success" />
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
  <img src="https://readme-typing-svg.demolab.com?font=Space+Mono&weight=700&size=18&duration=2400&pause=600&color=EF4444&center=true&vCenter=true&width=350&lines=RESPONS+ERROR;INFO+VALIDASI" alt="Error" />
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
  <img src="https://readme-typing-svg.demolab.com?font=Rajdhani&weight=700&size=28&duration=3800&pause=1400&color=F59E0B&center=true&vCenter=true&width=550&lines=STRUKTUR+NIK;PAHAMI+FORMATNYA" alt="NIK Format" />
</div>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Orbitron&weight=600&size=20&duration=2800&pause=900&color=8B5CF6&center=true&vCenter=true&width=650&lines=16+DIGIT+STRUKTUR;DECODE+SETIAP+BAGIAN" alt="Structure" />
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
  <img src="https://readme-typing-svg.demolab.com?font=Rajdhani&weight=700&size=28&duration=4000&pause=1500&color=06B6D4&center=true&vCenter=true&width=550&lines=PENGGUNAAN+LANJUTAN;SIAP+PRODUKSI" alt="Advanced Usage" />
</div>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Exo+2&weight=600&size=20&duration=2600&pause=800&color=8B5CF6&center=true&vCenter=true&width=450&lines=Backend+Node.js;Integrasi+Express" alt="Node.js" />
</div>

```javascript
const express = require('express');
const axios = require('axios');

const app = express();
app.use(express.json());

// Middleware validasi NIK
const validasiNIK = (req, res, next) => {
  const { nik } = req.body;
  
  if (!nik || !/^\d{16}$/.test(nik)) {
    return res.status(400).json({
      error: 'Format NIK tidak valid',
      message: 'NIK harus tepat 16 digit angka'
    });
  }
  
  next();
};

app.post('/api/nik/validasi', validasiNIK, async (req, res) => {
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
    
    // Tambahkan processing tambahan jika diperlukan
    const dataProses = {
      ...response.data,
      timestamp: new Date().toISOString(),
      source: 'NIK-Parse-API'
    };
    
    res.json(dataProses);
  } catch (error) {
    console.error('Error validasi NIK:', error.message);
    res.status(500).json({
      error: 'Service validasi tidak tersedia',
      message: 'Silakan coba lagi nanti'
    });
  }
});

const PORT = process.env.PORT || 3000;
app.listen(PORT, () => {
  console.log(`NIK Validation Service berjalan di port ${PORT}`);
});
```

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Exo+2&weight=600&size=20&duration=2600&pause=800&color=EC4899&center=true&vCenter=true&width=450&lines=React+Native;Pengembangan+Mobile" alt="React Native" />
</div>

```javascript
import React, { useState } from 'react';
import { View, Text, TextInput, TouchableOpacity, Alert } from 'react-native';

const ParserNIK = () => {
  const [nik, setNik] = useState('');
  const [hasil, setHasil] = useState(null);
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
        setHasil(data.data);
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
        Parser NIK Indonesia
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

      {hasil && (
        <View style={{ marginTop: 20 }}>
          <Text style={{ fontSize: 18, fontWeight: 'bold' }}>Hasil:</Text>
          <Text>Provinsi: {hasil.provinsi}</Text>
          <Text>Kab/Kota: {hasil.kotakab}</Text>
          <Text>Kecamatan: {hasil.kecamatan}</Text>
          <Text>Kelamin: {hasil.kelamin}</Text>
          <Text>Tanggal Lahir: {hasil.lahir}</Text>
        </View>
      )}
    </View>
  );
};

export default ParserNIK;
```

---

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Orbitron&weight=900&size=32&duration=4200&pause=1600&color=FF6B6B&center=true&vCenter=true&width=800&lines=Parsing+identitas+Indonesia+dengan+presisi;Membangun+jembatan+antara+data+dan+developer;Kode+yang+menghubungkan%2C+API+yang+memberdayakan;Inovasi+melalui+pemrosesan+data+cerdas" alt="Mission Statement" />
</div>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Exo+2&weight=700&size=22&duration=4500&pause=1800&color=00D4FF&center=true&vCenter=true&width=750&lines=🚀+Parser+NIK+super+cepat;🎯+Ekstraksi+data+akurat;🔒+Kebijakan+zero+data+retention;🌟+Dibuat+dengan+cinta+di+Indonesia" alt="Features Footer" />
</div>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Rajdhani&weight=600&size=18&duration=3500&pause=1200&color=10B981&center=true&vCenter=true&width=650&lines=Terima+kasih+telah+memilih+NIK+Parse+API;Beri+⭐+untuk+menunjukkan+dukungan;Follow+untuk+project+keren+lainnya;Selamat+coding%2C+developer+Indonesia!" alt="Gratitude" />
</div>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Space+Mono&weight=600&size=16&duration=5500&pause=2200&color=8B5CF6&center=true&vCenter=true&width=550&lines=©+2025+NIK+Parse+API;Open+source+•+MIT+Licensed;Dibuat+dengan+passion+•+Powered+by+Vercel" alt="Copyright" />
</div>
