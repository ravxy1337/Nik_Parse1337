<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Orbitron&weight=900&size=45&duration=3000&pause=1000&color=10B981&center=true&vCenter=true&width=700&lines=NIK+Parse+API;Parser+Identitas+Indonesia;Cepat+dan+Akurat;Siap+untuk+Produksi" alt="NIK Parse API" />
  
  <br><br>
  
  <p style="color: #059669; font-size: 18px; font-weight: 600;">
    Parse NIK Indonesia secara instan dengan ekstraksi informasi detail lengkap
  </p>
</div>

---

## <i class="fas fa-info-circle"></i> Apa itu NIK Parse?

**NIK (Nomor Induk Kependudukan)** adalah nomor identitas unik 16 digit yang dimiliki setiap warga negara Indonesia. NIK Parse adalah teknologi yang dapat mengekstrak informasi tersembunyi dari struktur NIK, meliputi:

- **<i class="fas fa-map-marker-alt"></i> Informasi Geografis**: Provinsi, Kabupaten/Kota, dan Kecamatan tempat NIK diterbitkan
- **<i class="fas fa-venus-mars"></i> Jenis Kelamin**: Berdasarkan kode tanggal lahir (01-31 untuk laki-laki, 41-71 untuk perempuan)
- **<i class="fas fa-calendar-alt"></i> Tanggal Lahir**: Ekstraksi tanggal, bulan, dan tahun kelahiran
- **<i class="fas fa-user-tag"></i> Kode Unik**: Nomor urut registrasi di wilayah tersebut
- **<i class="fas fa-plus-circle"></i> Data Tambahan**: Usia, zodiak, kode pos, dan informasi lainnya

### <i class="fas fa-cogs"></i> Cara Kerja NIK Parse

NIK memiliki struktur terorganisir: `XX.XXXX.DDMMYY.XXXX`
- **2 digit pertama**: Kode provinsi
- **4 digit berikutnya**: Kode kabupaten/kota dan kecamatan  
- **6 digit tengah**: Tanggal lahir (DD+40 untuk perempuan, MM, YY)
- **4 digit terakhir**: Nomor urut unik

API ini memparse struktur tersebut dan mencocokkannya dengan database wilayah Indonesia untuk memberikan informasi lengkap dan akurat.

---

<div align="center">
  <h2 style="color: #10B981; font-weight: 700;"><i class="fas fa-star"></i> FITUR UNGGULAN</h2>
</div>

<table align="center">
<tr>
<td align="center" width="50%">

<h4 style="color: #059669;"><i class="fas fa-bolt"></i> SUPER CEPAT</h4>

Parse NIK dalam hitungan milidetik dengan performa tinggi yang konsisten

</td>
<td align="center" width="50%">

<h4 style="color: #059669;"><i class="fas fa-bullseye"></i> AKURASI TINGGI</h4>

Validasi dan ekstraksi data yang sangat tepat dengan tingkat akurasi maksimal

</td>
</tr>
<tr>
<td align="center">

<h4 style="color: #059669;"><i class="fas fa-shield-alt"></i> KEAMANAN TINGGI</h4>

API yang aman dengan standar keamanan tingkat enterprise untuk data sensitif

</td>
<td align="center">

<h4 style="color: #059669;"><i class="fas fa-plug"></i> MUDAH INTEGRASI</h4>

REST API sederhana yang mudah diintegrasikan ke semua platform dan framework

</td>
</tr>
</table>

---

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Rajdhani&weight=700&size=30&duration=3200&pause=1100&color=10B981&center=true&vCenter=true&width=600&lines=PANDUAN+CEPAT" alt="Quick Start" />
</div>

### <i class="fas fa-link"></i> Base URL
\`\`\`
https://parse1337.vercel.app
\`\`\`

<div align="center">
  <h3 style="color: #10B981;"><i class="fas fa-code"></i> ENDPOINT API</h3>
</div>

| Metode | Endpoint | Deskripsi |
|--------|----------|-----------|
| **POST** | `/api/nik/parse` | Parse NIK menggunakan JSON payload |
| **GET** | `/api/nik/parse?nik=<nomor>` | Parse NIK menggunakan query parameter |

---

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Rajdhani&weight=700&size=28&duration=3400&pause=1200&color=10B981&center=true&vCenter=true&width=550&lines=CONTOH+KODE" alt="Code Examples" />
</div>

<div align="center">
  <h3 style="color: #059669;"><i class="fab fa-js-square"></i> Implementasi JavaScript</h3>
</div>

\`\`\`javascript
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
\`\`\`

<div align="center">
  <h3 style="color: #059669;"><i class="fas fa-terminal"></i> Perintah cURL</h3>
</div>

**POST Request**
\`\`\`bash
curl -X POST https://parse1337.vercel.app/api/nik/parse \
  -H "Content-Type: application/json" \
  -H "User-Agent: NIK-Parser/1.0" \
  -d '{"nik": "3201234567890001"}'
\`\`\`

**GET Request**
\`\`\`bash
curl "https://parse1337.vercel.app/api/nik/parse?nik=3201234567890001" \
  -H "Accept: application/json"
\`\`\`

<div align="center">
  <h3 style="color: #059669;"><i class="fab fa-python"></i> Implementasi Python</h3>
</div>

\`\`\`python
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
\`\`\`

<div align="center">
  <h3 style="color: #059669;"><i class="fab fa-react"></i> Komponen React</h3>
</div>

\`\`\`jsx
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
\`\`\`

---

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Rajdhani&weight=700&size=28&duration=3600&pause=1300&color=10B981&center=true&vCenter=true&width=550&lines=FORMAT+RESPONS" alt="Response Format" />
</div>

<div align="center">
  <h3 style="color: #059669;"><i class="fas fa-check-circle"></i> Respons Berhasil</h3>
</div>

\`\`\`json
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
\`\`\`

<div align="center">
  <h3 style="color: #059669;"><i class="fas fa-exclamation-triangle"></i> Respons Error</h3>
</div>

\`\`\`json
{
  "status": "error",
  "pesan": "NIK harus tepat 16 digit angka",
  "details": {
    "code": "INVALID_FORMAT",
    "received_length": 15,
    "expected_length": 16
  }
}
\`\`\`

---

<div align="center">
  <h2 style="color: #10B981; font-weight: 700;"><i class="fas fa-sitemap"></i> STRUKTUR NIK</h2>
</div>

<div align="center">
  <h3 style="color: #059669;"><i class="fas fa-hashtag"></i> 16 Digit Struktur</h3>
</div>

\`\`\`
Format NIK: XX.XXXX.DDMMYY.XXXX
            │  │    │      │
            │  │    │      └─── Nomor urut (0001-9999)
            │  │    └────────── Tanggal lahir (DDMMYY)
            │  └─────────────── Kode wilayah kecamatan  
            └────────────────── Kode provinsi & kabupaten/kota
\`\`\`

**<i class="fas fa-clipboard-list"></i> Contoh NIK Valid:**
- `3201234567890001` → Jawa Barat, Kabupaten Bogor
- `1101234567890001` → Aceh, Kabupaten Simeulue  
- `7371234567890001` → Sulawesi Selatan, Kota Makassar

### <i class="fas fa-info"></i> Penjelasan Detail Parsing

**1. Kode Wilayah (6 digit pertama)**
- 2 digit pertama: Kode provinsi (11=Aceh, 32=Jawa Barat, 73=Sulawesi Selatan)
- 2 digit berikutnya: Kode kabupaten/kota dalam provinsi
- 2 digit terakhir: Kode kecamatan dalam kabupaten/kota

**2. Tanggal Lahir (6 digit tengah)**
- 2 digit pertama: Tanggal (01-31 untuk laki-laki, 41-71 untuk perempuan)
- 2 digit berikutnya: Bulan (01-12)
- 2 digit terakhir: Tahun (2 digit terakhir tahun kelahiran)

**3. Nomor Urut (4 digit terakhir)**
- Nomor registrasi unik di wilayah tersebut (0001-9999)

---

<div align="center">
  <h2 style="color: #10B981; font-weight: 700;"><i class="fas fa-rocket"></i> PENGGUNAAN LANJUTAN</h2>
</div>

<div align="center">
  <h3 style="color: #059669;"><i class="fab fa-node-js"></i> Backend Node.js</h3>
</div>

\`\`\`javascript
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
\`\`\`

<div align="center">
  <h3 style="color: #059669;"><i class="fab fa-react"></i> React Native</h3>
</div>

\`\`\`javascript
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
\`\`\`

---

<div align="center">
  <h2 style="color: #10B981; font-weight: 700;"><i class="fas fa-question-circle"></i> FAQ & TROUBLESHOOTING</h2>
</div>

### <i class="fas fa-question"></i> Pertanyaan Umum

**Q: Apakah API ini menyimpan data NIK yang diparse?**
A: Tidak, API ini tidak menyimpan data NIK apapun. Semua proses parsing dilakukan secara real-time tanpa penyimpanan.

**Q: Berapa batas rate limit untuk API ini?**
A: Saat ini belum ada rate limit yang diberlakukan, namun gunakan dengan bijak untuk performa optimal.

**Q: Apakah bisa parse NIK yang tidak valid?**
A: API akan mengembalikan error jika format NIK tidak sesuai (bukan 16 digit atau mengandung karakter non-numerik).

### <i class="fas fa-tools"></i> Troubleshooting

**Error: "NIK harus tepat 16 digit angka"**
- Pastikan NIK yang dikirim tepat 16 digit
- Hapus spasi, tanda hubung, atau karakter non-numerik

**Error: "Gagal terhubung ke server"**
- Periksa koneksi internet
- Pastikan URL endpoint benar
- Coba lagi setelah beberapa saat

---

<div align="center">
  <h2 style="color: #10B981; font-weight: 700;"><i class="fas fa-heart"></i> KONTRIBUSI & DUKUNGAN</h2>
</div>

<div align="center">
  <p style="color: #059669; font-size: 16px;">
    <i class="fas fa-envelope"></i> Untuk pertanyaan, saran, atau laporan bug, silakan hubungi developer
  </p>
  
  <p style="color: #059669; font-size: 14px;">
    <i class="fas fa-code"></i> Dibuat dengan <i class="fas fa-heart" style="color: #e74c3c;"></i> untuk kemudahan akses data kependudukan Indonesia
  </p>
</div>

---

<div align="center">
  <p style="color: #6b7280; font-size: 12px;">
    <i class="fas fa-shield-alt"></i> API ini dibuat untuk tujuan edukasi dan pengembangan. 
    Pastikan mematuhi regulasi perlindungan data pribadi yang berlaku.
  </p>
</div>
