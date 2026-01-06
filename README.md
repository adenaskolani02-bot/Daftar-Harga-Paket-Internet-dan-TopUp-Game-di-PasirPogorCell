<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cek Daftar Harga di PasirPogorCell</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            background: linear-gradient(135deg, #f0f4ff 0%, #e0f2fe 100%);
            min-height: 100vh;
        }
        .card {
            background: linear-gradient(135deg, #ffffff 0%, #f8fafc 100%);
            border-radius: 12px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            padding: 20px;
            margin-bottom: 20px;
            border: 1px solid #e2e8f0;
        }
        .header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 30px;
            text-align: center;
            border-radius: 12px 12px 0 0;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        .tab-button {
            padding: 12px 24px;
            cursor: pointer;
            border-radius: 8px 8px 0 0;
            transition: all 0.3s ease;
            font-weight: 500;
        }
        .tab-button.active {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
        }
        .tab-button:hover {
            background: linear-gradient(135deg, #764ba2 0%, #667eea 100%);
        }
        .operator-button, .game-button {
            padding: 10px 18px;
            margin-right: 10px;
            cursor: pointer;
            border-radius: 8px;
            transition: all 0.3s ease;
            font-weight: 500;
            background: #e2e8f0;
            color: #374151;
        }
        .operator-button.active, .game-button.active {
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            color: white;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
        }
        .operator-button:hover, .game-button:hover {
            background: linear-gradient(135deg, #f5576c 0%, #f093fb 100%);
            color: white;
        }
        .hidden {
            display: none;
        }
        .info-toko {
            background: linear-gradient(135deg, #a8edea 0%, #fed6e3 100%);
            border-radius: 12px;
            padding: 20px;
            margin: 20px 0;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        .price-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 12px;
        }
        .price-item {
            background: #f8fafc;
            border-radius: 8px;
            padding: 10px;
            border-left: 4px solid #667eea;
        }
        .price-item li {
            list-style: none;
            font-weight: 400;
        }
    </style>
</head>
<body>
    <div class="container mx-auto p-4">
        <div class="header">
            <h1 class="text-4xl font-bold">Cek Daftar Harga di PasirPogorCell</h1>
        </div>

        <!-- Bagian Info Toko dengan Alamat -->
        <div class="info-toko">
            <h2 class="text-2xl font-semibold text-center mb-4 text-gray-800">Info Toko PasirPogorCell</h2>
            <div class="text-center">
                <p class="text-gray-700 mb-2 font-medium"><strong>Alamat:</strong> Pasir Pogor, RT.2/RW.1, Ciparasi, Kec. Sobang, Kabupaten Lebak, Banten 42280</p>
                <p class="text-gray-700 mb-2 font-medium"><strong>Telepon:</strong> (+62) 838-4484-3020</p>
                <p class="text-gray-700 font-medium">Kunjungi kami untuk layanan terbaik!</p>
            </div>
        </div>

        <div class="flex mt-4 bg-gray-200 rounded-t-lg overflow-x-auto">
            <div class="tab-button active" onclick="showTab('internet')">Paket Internet</div>
            <div class="tab-button" onclick="showTab('game')">Daftar Harga TopUp Game</div>
        </div>

        <!-- Paket Internet Section -->
        <div id="internet-tab">
            <div class="flex mt-4 overflow-x-auto bg-gray-100 p-2 rounded">
                <div class="operator-button active" onclick="showOperator('indosat')">Indosat</div>
                <div class="operator-button" onclick="showOperator('axis')">Axis</div>
                <div class="operator-button" onclick="showOperator('telkomsel')">Telkomsel</div>
                <div class="operator-button" onclick="showOperator('byu')">byU</div>
            </div>
            
            <!-- Indosat Content -->
            <div id="indosat-content" class="operator-content">
                <div class="mt-8">
                    <h2 class="text-2xl font-semibold mb-4">Paket Internet Harian</h2>
                    <div class="card">
                        <h3 class="font-bold">Indosat Yellow:</h3>
                        <div class="price-list">
                            <div class="price-item"><li>Indosat Yellow 1GB 1 Hari - Rp 8.000</li></div>
                            <div class="price-item"><li>Indosat Yellow 1GB 2 Hari - Rp 9.000</li></div>
                            <div class="price-item"><li>Indosat Yellow 1GB 7 Hari - Rp 10.000</li></div>
                            <div class="price-item"><li>Indosat Yellow 1GB 15 Hari - Rp 12.000</li></div>
                        </div>
                    </div>
                    <div class="card">
                        <h3 class="font-bold">Freedom Mini Data:</h3>
                        <div class="price-list">
                            <div class="price-item"><li>Freedom Mini 3GB 1 Hari - Rp 10.000</li></div>
                            <div class="price-item"><li>Freedom Mini 5GB 2 Hari - Rp 12.000</li></div>
                            <div class="price-item"><li>Freedom Mini 3GB 3 Hari - Rp 15.000</li></div>
                            <div class="price-item"><li>Freedom Mini 2,5GB 5 Hari (Unreg) - Rp 16.000</li></div>
                            <div class="price-item"><li>Freedom Mini 3,5GB 5 Hari - Rp 17.000</li></div>
                            <div class="price-item"><li>Freedom Mini 5GB 5 Hari (Unreg) - Rp 20.000</li></div>
                            <div class="price-item"><li>Freedom Mini 7GB 7 Hari - Rp 26.000</li></div>
                            <div class="price-item"><li>Freedom Mini 15GB 7 Hari - Rp 32.000</li></div>
                        </div>
                    </div>
                </div>

                <div class="mt-8">
                    <h2 class="text-2xl font-semibold mb-4">Paket Internet Bulanan</h2>
                    <div class="card">
                        <h3 class="font-bold">Pure Mini Data:</h3>
                        <div class="price-list">
                            <div class="price-item"><li>100MB 24 Jam 30 Hari - Rp 2.000</li></div>
                            <div class="price-item"><li>200MB 24 Jam 30 Hari - Rp 3.000</li></div>
                            <div class="price-item"><li>250MB 24 Jam 30 Hari - Rp 3.500</li></div>
                            <div class="price-item"><li>300MB 24 Jam 30 Hari - Rp 4.000</li></div>
                            <div class="price-item"><li>400MB 24 Jam 30 Hari - Rp 5.000</li></div>
                            <div class="price-item"><li>500MB 24 Jam 30 Hari - Rp 6.000</li></div>
                            <div class="price-item"><li>600MB 24 Jam 30 Hari - Rp 7.000</li></div>
                            <div class="price-item"><li>700MB 24 Jam 30 Hari - Rp 8.000</li></div>
                            <div class="price-item"><li>800MB 24 Jam 30 Hari - Rp 8.500</li></div>
                            <div class="price-item"><li>1GB All Jaringan 30 Hari - Rp 9.000</li></div>
                            <div class="price-item"><li>1,5GB All Jaringan 30 Hari - Rp 13.000</li></div>
                            <div class="price-item"><li>2GB All Jaringan 30 Hari - Rp 16.000</li></div>
                            <div class="price-item"><li>2,5 GB All Jaringan 30 Hari - Rp 20.000</li></div>
                            <div class="price-item"><li>3GB All Jaringan 30 Hari - Rp 22.000</li></div>
                            <div class="price-item"><li>4GB All Jaringan 30 Hari - Rp 28.000</li></div>
                        </div>
                    </div>
                    <div class="card">
                        <h3 class="font-bold">Freedom Internet:</h3>
                        <div class="price-list">
                            <div class="price-item"><li>Freedom Internet 3GB 28 Hari - Rp 23.000</li></div>
                            <div class="price-item"><li>Freedom Internet 4GB 28 Hari - Rp 29.000</li></div>
                            <div class="price-item"><li>Freedom Internet 5.5GB 28 Hari - Rp 33.000</li></div>
                            <div class="price-item"><li>Freedom Internet 9GB 28 Hari - Rp 44.000</li></div>
                            <div class="price-item"><li>Freedom Internet 13GB 28 Hari - Rp 57.000</li></div>
                            <div class="price-item"><li>Freedom Internet 16GB 28 Hari - Rp 69.000</li></div>
                            <div class="price-item"><li>Freedom Internet 20GB 28 Hari - Rp 71.000</li></div>
                            <div class="price-item"><li>Freedom Internet 25GB 28 Hari - Rp 83.000</li></div>
                            <div class="price-item"><li>Freedom Internet 30GB 28 Hari - Rp 97.000</li></div>
                            <div class="price-item"><li>Freedom Internet 42GB 28 Hari - Rp 105.000</li></div>
                            <div class="price-item"><li>Freedom Internet Sensasi 50GB 28 Hari - Rp 106.000</li></div>
                            <div class="price-item"><li>Freedom Internet Sensasi 70GB 28 Hari - Rp 127.000</li></div>
                            <div class="price-item"><li>Freedom Internet Sensasi 150 GB 28 Hari - Rp 160.000</li></div>
                            <div class="price-item"><li>Freedom Internet Sensasi 200GB 28 Hari - Rp 201.000</li></div>
                        </div>
                    </div>
                </div>

                <div class="mt-8">
                    <h2 class="text-2xl font-semibold mb-4">Paket Unlimited</h2>
                    <div class="card">
                        <h3 class="font-bold">Freedom Unlimited:</h3>
                        <div class="price-list">
                            <div class="price-item"><li>1GB + 2GB + Unlimited App 6 Hari - Rp 20.000</li></div>
                            <div class="price-item"><li>1GB All + 4,5GB + Unlimited App 28 Hari - Rp 36.000</li></div>
                            <div class="price-item"><li>2GB All + 7,5 s/d 8GB + Unli App 28 Hari - Rp 59.000</li></div>
                            <div class="price-item"><li>3GB All + 15 s/d 17GB + Unli App 28 Hari - Rp 83.000</li></div>
                            <div class="price-item"><li>7GB All + 28GB + Unlimited App 28 Hari - Rp 108.000</li></div>
                            <div class="price-item"><li>10GB All + 35GB + Unlimited App 28 Hari - Rp 120.000</li></div>
                            <div class="price-item"><li>15GB All + 25GB + Unlimited App, Telp & SMS 28 Hari - Rp 131.000</li></div>
                            <div class="price-item"><li>Unlimited (90GB All + Unl App + Telp + SMS) 24 jam 28 Hari - Rp 162.000</li></div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Axis Content -->
            <div id="axis-content" class="operator-content hidden">
                <div class="mt-8">
                    <h2 class="text-2xl font-semibold mb-4">Paket Internet Harian</h2>
                    <div class="card">
                        <h3 class="font-bold">Aigo Kuota Mini:</h3>
                        <div class="price-list">
                            <div class="price-item"><li>Mini 1,5GB + Bonus Aigo 1 Hari - Rp 8.000</li></div>
                            <div class="price-item"><li>Mini Axis 2,5GB + Bonus Aigo 1 Hari - Rp 10.000</li></div>
                            <div class="price-item"><li>Mini Axis 2GB + Bonus Aigo 3 Hari - Rp 12.000</li></div>
                            <div class="price-item"><li>Mini Axis 2,5GB + Bonus Aigo 3 Hari - Rp 13.000</li></div>
                            <div class="price-item"><li>Mini Axis 3GB + Bonus Aigo 3 Hari - Rp 13.000</li></div>
                            <div class="price-item"><li>Mini Axis 4,5GB + Bonus Aigo 3 Hari - Rp 15.000</li></div>
                            <div class="price-item"><li>Mini Axis 9GB + Bonus Aigo 3 Hari - Rp 17.000</li></div>
                        </div>
                    </div>
                </div>

                <div class="mt-8">
                    <h2 class="text-2xl font-semibold mb-4">Paket Internet Per Jam</h2>
                    <div class="card">
                        <h3 class="font-bold">Axis Paket Data Warnet:</h3>
                        <div class="price-list">
                            <div class="price-item"><li>Axis Data Paket Warnet 800 MB (1 Jam) - Rp 3.000</li></div>
                            <div class="price-item"><li>Axis Data Paket Warnet Unlimited 1 Jam - Rp 4.000</li></div>
                            <div class="price-item"><li>Axis Data Paket Warnet 1,5 GB (2 Jam) - Rp 4.000</li></div>
                            <div class="price-item"><li>Axis Data Paket Warnet 3 GB (3 Jam) - Rp 5.000</li></div>
                            <div class="price-item"><li>Axis Data Paket Warnet Unlimited 3 Jam - Rp 6.000</li></div>
                            <div class="price-item"><li>Axis Data Paket Warnet 3 GB (6 Jam) - Rp 7.000</li></div>
                            <div class="price-item"><li>Axis Data Paket Warnet Unlimited 24 Jam - Rp 10.000</li></div>
                        </div>
                    </div>
                </div>

                <div class="mt-8">
                    <h2 class="text-2xl font-semibold mb-4">Paket Internet Bulanan (30 Hari)</h2>
                    <div class="card">
                        <h3 class="font-bold">Bronet Bulanan:</h3>
                        <div class="price-list">
                            <div class="price-item"><li>Axis Data 1GB All 30 Hari - Rp 10.000</li></div>
                            <div class="price-item"><li>Bronet 2GB + Bonus Aigo 30 Hari - Rp 18.000</li></div>
                            <div class="price-item"><li>Bronet 3GB + Bonus Aigo 30 Hari - Rp 21.000</li></div>
                            <div class="price-item"><li>Bronet 6GB + Bonus Aigo 30 Hari - Rp 32.000</li></div>
                            <div class="price-item"><li>Bronet 8GB + Bonus Aigo 30 Hari - Rp 41.000</li></div>
                            <div class="price-item"><li>Bronet 14GB + Bonus Aigo 30 Hari - Rp 62.000</li></div>
                            <div class="price-item"><li>Axis Data Bronet 16GB All 30 Hari - Rp 74.000</li></div>
                            <div class="price-item"><li>Bronet 20GB + Bonus Aigo 30 Hari - Rp 74.000</li></div>
                            <div class="price-item"><li>Bronet 30GB + Bonus Aigo 30 Hari - Rp 91.000</li></div>
                        </div>
                    </div>
                </div>

                <div class="mt-8">
                    <h2 class="text-2xl font-semibold mb-4">Paket Internet Bulanan (60 Hari)</h2>
                    <div class="card">
                        <h3 class="font-bold">Bronet Bulanan:</h3>
                        <div class="price-list">
                            <div class="price-item"><li>Bronet 2GB All 24 Jam 60 Hari - Rp 32.000</li></div>
                            <div class="price-item"><li>Bronet 3GB All 24 Jam 60 Hari - Rp 41.000</li></div>
                            <div class="price-item"><li>Bronet 5GB All 24 Jam 60 Hari - Rp 58.000</li></div>
                            <div class="price-item"><li>Bronet 8GB All 24 Jam 60 Hari - Rp 78.000</li></div>
                            <div class="price-item"><li>Bronet 10GB All 24 Jam 60 Hari - Rp 89.000</li></div>
                            <div class="price-item"><li>Bronet 12GB All 24 Jam 60 Hari - Rp 100.000</li></div>
                            <div class="price-item"><li>Bronet 35GB + Bonus Aigo 60 Hari - Rp 110.000</li></div>
                            <div class="price-item"><li>Bronet 16GB All 24 Jam 60 Hari - Rp 119.000</li></div>
                            <div class="price-item"><li>Bronet 75GB + Bonus Aigo 60 Hari - Rp 171.000</li></div>
                        </div>
                    </div>
                </div>

                <div class="mt-8">
                    <h2 class="text-2xl font-semibold mb-4">Paket Kuota Games 30 Hari</h2>
                    <div class="card">
                        <h3 class="font-bold">Paket Kuota Games:</h3>
                        <ul class="list-disc pl-5">
                            <li>Kuota Games Only 1GB 30 Hari - Rp 7.000</li>
                            <li>500MB All + 500MB Kuota Game 30 Hari - Rp 9.000</li>
                            <li>Kuota Games Only 2GB 30 Hari - Rp 11.000</li>
                            <li>1GB All + 1GB Kuota Game 30 Hari - Rp 14.000</li>
                            <li>1,5GB All + 1,5GB Kuota Game 30 Hari - Rp 17.000</li>
                            <li>1GB All + 1GB 4G +2GB Game 30 Hari - Rp 21.000</li>
                            <li>2GB All + 2GB Kuota Game 30 Hari - Rp 23.000</li>
                            <li>1GB All + 3GB 4G + 4GB Game 30 Hari - Rp 35.000</li>
                        </ul>
                    </div>
                </div>
            </div>

<!-- Telkomsel Content -->
<div id="telkomsel-content" class="operator-content hidden">
    <div class="mt-8">
        <h2 class="text-2xl font-semibold mb-4">Paket Internet Harian</h2>
        <div class="card">
            <h3 class="font-bold">Data Mini Harian:</h3>
            <ul class="list-disc pl-5">
                <li>Mini Data 1GB AII 1 Hari - Rp 10.000</li>
                <li>Mini Data 500MB AIl 3 Hari - Rp 10.000</li>
                <li>(Non-Pamasuka) Mini Data 1,5GB All 3 Hari - Rp 13.000</li>
                <li>Mini Data 1GB AIl 3 Hari - Rp 13.000</li>
                <li>Mini Data 2,5GB All 5 Hari - Rp 15.000</li>
                <li>Mini Data 2GB AIl 3 Hari - Rp 15.000</li>
                <li>Mini Data 2.5GB - 3GB All 5 Hari - Rp 16.000</li>
                <li>Mini Data 4GB AII 1 Hari - Rp 12.550</li>
                <li>Mini Data 6GB AIl 1 Hari - Rp 23.000</li>
                <li>Mini Data 5GB All 1 Hari - Rp 25.000</li>
                <li>Mini Data 3GB All 3 Hari - Rp 27.000</li>
                <li>Mini Data 5GB All 3 Hari - Rp 34.000</li>
                <li>Mini Data 8GB AII 3 Hari - Rp 40.000</li>
                <li>Mini Data 7GB AII 3 Hari - Rp 50.000</li>
                <li>Mini Data 17GB AII 3 Hari - Rp 64.000</li>
                <li>Mini Data 15GB AIl 3 Hari - Rp 66.000</li>
                <li>Mini Data 20GB AIl 3 Hari - Rp 74.000</li>
                <li>Mini Data 10GB AIl 3 Hari - Rp 78.000</li>
            </ul>
        </div>
    </div>

    <div class="mt-8">
        <h2 class="text-2xl font-semibold mb-4">Paket Internet Mingguan</h2>
        <div class="card">
            <h3 class="font-bold">Data Mini Mingguan:</h3>
            <ul class="list-disc pl-5">
                <li>Tsel Mini Data 50MB 7 Hari - Rp 4.000</li>
                <li>Tsel Mini Data 100MB 7 Hari - Rp 7.000</li>
                <li>Tsel Mini Data 250MB 7 Hari - Rp 8.000</li>
                <li>Tsel Mini Data 500MB 7 Hari - Rp 10.000</li>
                <li>Mini Data 500MB All 7 Hari - Rp 11.000</li>
                <li>Mini Data 1GB AII 7 Hari - Rp 13.000</li>
                <li>1GB All Jaringan 30 Hari - Rp 15.000</li>
                <li>Tsel Mini Data 750MB 7 Hari - Rp 18.000</li>
                <li>Mini Data 2GB AIl 7 Hari - Rp 19.000</li>
                <li>Mini Data 3GB All 7 Hari - Rp 24.000</li>
                <li>Mini Data 2GB All 14 Hari - Rp 25.000</li>
                <li>Mini Data 5GB All 7 Hari - Rp 29.000</li>
                <li>Mini Data 7GB All 7 Hari - Rp 30.000</li>
                <li>Mini Data 17GB All 7 Hari - Rp 80.000</li>
            </ul>
        </div>
    </div>

    <div class="mt-8">
        <h2 class="text-2xl font-semibold mb-4">Paket Mini Data Lokal</h2>
        <div class="card">
            <h3 class="font-bold">Data Mini Jabo - Banten:</h3>
            <ul class="list-disc pl-5">
                <li>Data 1,5GB 3 Hari - Rp 11.000</li>
                <li>Data 2,5GB 5 Hari - Rp 14.000</li>
                <li>Data 3GB 3 Hari - Rp 15.000</li>
                <li>Data 3GB 5 Hari - Rp 16.000</li>
                <li>Data 3,5GB 7 Hari - Rp 22.000</li>
                <li>Data 4,5GB 5 Hari - Rp 23.000</li>
                <li>Data 5,5GB 5 Hari - Rp 27.000</li>
                <li>Data 5GB 7 Hari - Rp 29.000</li>
                <li>Data 7GB 7 Hari - Rp 30.000</li>    
                <li>Data 0,5GB All+ 1,5GB Lokal + 2GB OMG 30 Hari - Rp 36.000</li>
                <li>Data 10GB 7 Hari - Rp 39.000</li>
                <li>Data 12GB 7 Hari - Rp 44.000</li>
                <li>Data 1,25GB All + 3,75GB Lokal + 2GB OMG 30 Hari - Rp 50.000</li>
                <li>Data 2GB All + 6GB Lokal + 2GB OMG 30 Hari - Rp 65.000</li>
                <li>Data 3GB All + 9GB Lokal + 2GB OMG 30 Hari - Rp 74.000</li>
                <li>Data 4,5GB All + 13,5GB Lokal + 2GB OMG 30 Hari - Rp 85.000</li>
                <li>Data 5GB+ 37GB Lokal Jabo - Jabar 30 Hari - Rp 101.000</li>
                <li>Data 6GB + 54GB Lokal Jabo - Jabar 30 Hari - Rp 141.000</li>
                <li>Data 9GB + 71GB Lokal Jabo - Jabar 30 Hari - Rp 170.000</li>
            </ul>
        </div>
    </div>
</div>

<!-- ByU Content -->
<div id="byu-content" class="operator-content hidden">
    <div class="mt-8">
        <h2 class="text-2xl font-semibold mb-4">Paket Data ByU</h2>
        <div class="card">
            <h3 class="font-bold">Paket Data Harian:</h3>
            <ul class="list-disc pl-5">
                <li>1GB All + Bebas Tiktok 500MB/ Hari 1 Hari - Rp 8.000</li>
                <li>Kuota 2GB All 1 Hari - Rp 10.000</li>
                <li>2GB All + Bebas Tiktok 500MB/ Hari 3 Hari - Rp 12.000</li>
                <li>10GB All + Bebas Tiktok 500MB/ Hari 1 Hari - Rp 14.000</li>
                <li>Kuota 2,5GB All 5 Hari - Rp 14.000</li>
                <li>Kuota 3GB All 7 Hari - Rp 16.000</li>
                <li>ByU Yang Bikin Deket 3GB - 1 Hari - Rp 21.000</li>
                <li>Kuota 5GB All 7 Hari - Rp 21.000</li>
            </ul>
        </div>
    </div>
</div>

            <!-- byU Content -->
            <div id="byu-content" class="operator-content hidden">
                <div class="card mt-8">
                    <h3 class="text-xl font-semibold">Daftar Harga byU</h3>
                    <p class="text-gray-600 mt-2">Data harga byU akan ditampilkan di sini</p>
                </div>
            </div>
        </div>

        <!-- Game TopUp Section -->
        <div id="game-tab" class="hidden">
            <div class="flex mt-4 overflow-x-auto">
                <div class="game-button active" onclick="showGame('mobile-legends')">Mobile Legends</div>
                <div class="game-button" onclick="showGame('free-fire')">Free Fire</div>
            </div>

            
<!-- Mobile Legends Content -->
<div id="mobile-legends-content" class="game-content">
    <div class="card mt-8">
        <h3 class="text-xl font-semibold mb-4">Daftar Harga TopUp Mobile Legends</h3>
        
        <div class="space-y-4">
            <div class="border-b pb-2">
                <p class="font-medium">3 Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 3.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">5 Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 4.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">12(11+1) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 7.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">19(17+2) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 10.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">28(25+3) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 11.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">36(33+3) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 13.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">44(40+4) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 15.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">56(51+5) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 19.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">59(53+6) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 20.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">74(69+5) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 23.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">85(77+8) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 27.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">86(78+8) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 27.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">100 Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 31.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">1X Weekly Diamond Pass 220 (80+20/Hari)</p>
                <p class="text-gray-600">Rp 31.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">112(102+10) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 34.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">144(130+14) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 42.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">170(154+16) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 50.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">172(156+16) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 50.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">185(167+18) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 54.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">2X Weekly Diamond Pass 440 (80+20/Hari)</p>
                <p class="text-gray-600">Rp 60.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">222(200+22) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 63.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">229(207+22) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 66.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">240(217+23) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 69.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">257(234+23) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 72.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">Mobile Legend Coupon Pass</p>
                <p class="text-gray-600">Rp 76.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">278(251+27) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 79.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">284(254+30) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 80.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">296(256+40) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 82.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">301(261+40) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 84.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">Starlight Membership</p>
                <p class="text-gray-600">Rp 85.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">3X Weekly Diamond Pass 660 (80+20/Hari)</p>
                <p class="text-gray-600">Rp 87.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">344(312+32) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 96.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">345(301+44) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 97.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">355(309+46) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 100.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">374(326+48) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 106.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">381(333+48) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 107.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">384 Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 110.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">408(367+41) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 114.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">4X Weekly Diamond Pass 880 (80+20/Hari)</p>
                <p class="text-gray-600">Rp 15.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">429(390+39) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 118.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">425(373+52) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 120.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">448 Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 137.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">460 Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 140.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">514(468+46) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 142.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">5X Weekly Diamond Pass 1100 (80+20/Hari)</p>
                <p class="text-gray-600">Rp 143.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">522(471+51) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 146.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">500 Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 150.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">Mobile Legend Twilight Pass</p>
                <p class="text-gray-600">Rp 155.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">568(503+65) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 155.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">601(533+68) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 165.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">642 Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 185.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">706(625+81) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 200.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">712(633+79) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 201.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">717(638+79) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 203.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">Starlight Member Plus</p>
                <p class="text-gray-600">Rp 220.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">875(774+101) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 240.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">965(856+109) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 264.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">963(859+104) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 265.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">977(867+110) Diamond Mobile Legend</p>
                <p class="text-gray-600">Rp 268.000</p>
            </div>
        </div>
    </div>
</div>

<!-- Free Fire Content -->
<div id="free-fire-content" class="game-content hidden">
    <div class="card mt-8">
        <h3 class="text-xl font-semibold mb-4">Daftar Harga TopUp Free Fire</h3>
        
        <div class="space-y-4">
            <div class="border-b pb-2">
                <p class="font-medium">5 Diamond Free Fire</p>
                <p class="text-gray-600">Rp 3.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">12 Diamond Free Fire</p>
                <p class="text-gray-600">Rp 4.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">50 Diamond Free Fire</p>
                <p class="text-gray-600">Rp 10.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">70 Diamond Free Fire</p>
                <p class="text-gray-600">Rp 12.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">100 Diamond Free Fire</p>
                <p class="text-gray-600">Rp 16.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">Membership Level Up Pass</p>
                <p class="text-gray-600">Rp 17.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">140 Diamond Free Fire</p>
                <p class="text-gray-600">Rp 21.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">210 Diamond Free Fire</p>
                <p class="text-gray-600">Rp 30.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">Membership Mingguan 50 Diamond</p>
                <p class="text-gray-600">Rp 31.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">300 Diamond Free Fire</p>
                <p class="text-gray-600">Rp 43.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">Booyah Pass (BP CARD)</p>
                <p class="text-gray-600">Rp 45.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">355 Diamond Free Fire</p>
                <p class="text-gray-600">Rp 50.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">500 Diamond Free Fire</p>
                <p class="text-gray-600">Rp 70.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">Membership Bulanan 50 Diamond</p>
                <p class="text-gray-600">Rp 86.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">720 Diamond Free Fire</p>
                <p class="text-gray-600">Rp 92.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">1000 Diamond Free Fire</p>
                <p class="text-gray-600">Rp 132.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">1450 Diamond Free Fire</p>
                <p class="text-gray-600">Rp 190.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">2180 Diamond Free Fire</p>
                <p class="text-gray-600">Rp 290.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">3640 Diamond Free Fire</p>
                <p class="text-gray-600">Rp 480.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">4000 Diamond Free Fire</p>
                <p class="text-gray-600">Rp 530.000</p>
            </div>
            
            <div class="border-b pb-2">
                <p class="font-medium">7290 Diamond Free Fire</p>
                <p class="text-gray-600">Rp 950.000</p>
            </div>
        </div>
    </div>
</div>

    <script>
        // Tab navigation
        function showTab(tabName) {
            // Hide all tabs
            document.getElementById('internet-tab').classList.add('hidden');
            document.getElementById('game-tab').classList.add('hidden');
            
            // Show selected tab
            document.getElementById(tabName + '-tab').classList.remove('hidden');
            
            // Update active button
            const tabButtons = document.querySelectorAll('.tab-button');
            tabButtons.forEach(button => {
                button.classList.remove('active');
            });
            event.currentTarget.classList.add('active');
        }

        // Operator navigation
        function showOperator(operatorName) {
            // Hide all operator contents
            const operatorContents = document.querySelectorAll('.operator-content');
            operatorContents.forEach(content => {
                content.classList.add('hidden');
            });
            
            // Show selected operator content
            document.getElementById(operatorName + '-content').classList.remove('hidden');
            
            // Update active button
            const operatorButtons = document.querySelectorAll('.operator-button');
            operatorButtons.forEach(button => {
                button.classList.remove('active');
            });
            event.currentTarget.classList.add('active');
        }

        // Game navigation
        function showGame(gameName) {
            // Hide all game contents
            const gameContents = document.querySelectorAll('.game-content');
            gameContents.forEach(content => {
                content.classList.add('hidden');
            });
            
            // Show selected game content
            document.getElementById(gameName + '-content').classList.remove('hidden');
            
            // Update active button
            const gameButtons = document.querySelectorAll('.game-button');
            gameButtons.forEach(button => {
                button.classList.remove('active');
            });
            event.currentTarget.classList.add('active');
        }
    </script>
</body>
</html>
