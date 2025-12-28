# qc-control-atratab
فرم کنترل کیفی شرکت آترا طب قومس
[deepseek_html_20251228_53ba6c (3).html](https://github.com/user-attachments/files/24362339/deepseek_html_20251228_53ba6c.3.html)
<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>کنترل کیفی تجهیزات پزشکی - شرکت آترا طب قومس</title>
    <style>
        * {
            font-family: 'B Nazanin', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        
        body {
            background: linear-gradient(135deg, #f0f4f8 0%, #dfe7f0 100%);
            padding: 15px;
            color: #2c3e50;
            line-height: 1.6;
            min-height: 100vh;
        }
        
        .container {
            max-width: 1350px;
            margin: 0 auto;
            background-color: white;
            border-radius: 12px;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1);
            padding: 0;
            overflow: hidden;
        }
        
        /* هدر شرکت */
        .company-header {
            background: linear-gradient(135deg, #1a237e 0%, #283593 100%);
            color: white;
            padding: 25px 30px;
            text-align: center;
            border-bottom: 5px solid #ff5252;
            position: relative;
            overflow: hidden;
        }
        
        .company-header::before {
            content: "";
            position: absolute;
            top: -50%;
            right: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 1px, transparent 1px);
            background-size: 25px 25px;
            opacity: 0.15;
            z-index: 0;
        }
        
        .company-name {
            font-size: 28px;
            font-weight: bold;
            letter-spacing: 0.5px;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.3);
            margin-bottom: 8px;
            position: relative;
            z-index: 1;
        }
        
        .company-subtitle {
            font-size: 18px;
            font-weight: 500;
            opacity: 0.95;
            color: #ffcc80;
            margin-bottom: 10px;
            position: relative;
            z-index: 1;
        }
        
        .company-info {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 15px;
            font-size: 14px;
            opacity: 0.9;
            position: relative;
            z-index: 1;
        }
        
        .info-item {
            display: flex;
            align-items: center;
            gap: 8px;
            background: rgba(255, 255, 255, 0.12);
            padding: 6px 15px;
            border-radius: 20px;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .info-item i {
            color: #ffcc80;
            font-size: 16px;
        }
        
        /* بخش فرم */
        .form-container {
            padding: 25px;
        }
        
        .form-title {
            text-align: center;
            color: #1a237e;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 2px solid #e8eaf6;
            font-size: 22px;
            position: relative;
            font-weight: bold;
        }
        
        .form-title::after {
            content: "";
            position: absolute;
            bottom: -2px;
            right: 50%;
            transform: translateX(50%);
            width: 120px;
            height: 3px;
            background: #ff5252;
        }
        
        .header-section {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 25px;
            flex-wrap: wrap;
            gap: 20px;
            background: #f5f7ff;
            padding: 20px;
            border-radius: 10px;
            border: 1px solid #e1e8ff;
        }
        
        .center-info {
            display: flex;
            gap: 25px;
            flex-wrap: wrap;
            flex-grow: 1;
        }
        
        .center-info-item {
            display: flex;
            flex-direction: column;
            gap: 8px;
            min-width: 250px;
        }
        
        .center-info-item label {
            font-weight: 600;
            color: #1a237e;
            font-size: 14px;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .center-info-item label::before {
            content: "•";
            color: #ff5252;
            font-size: 18px;
        }
        
        input[type="text"], input[type="number"], select, textarea {
            width: 100%;
            padding: 10px 12px;
            border: 1px solid #ced4da;
            border-radius: 6px;
            font-size: 14px;
            transition: all 0.3s;
            background-color: #fff;
        }
        
        input[type="text"]:focus, input[type="number"]:focus, select:focus, textarea:focus {
            outline: none;
            border-color: #5c6bc0;
            box-shadow: 0 0 0 3px rgba(92, 107, 192, 0.1);
        }
        
        textarea {
            resize: vertical;
            min-height: 60px;
            font-family: inherit;
        }
        
        /* جدول */
        .table-container {
            overflow-x: auto;
            margin-top: 20px;
            border-radius: 8px;
            border: 1px solid #e1e8ff;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
            min-width: 1250px;
        }
        
        th {
            background: linear-gradient(to bottom, #3f51b5, #303f9f);
            color: white;
            font-weight: 600;
            text-align: center;
            padding: 16px 10px;
            border: 1px solid #3949ab;
            white-space: nowrap;
            font-size: 14px;
            position: sticky;
            top: 0;
            z-index: 10;
        }
        
        td {
            padding: 12px 8px;
            border: 1px solid #e1e1e1;
            text-align: center;
            vertical-align: middle;
            background-color: #fff;
            font-size: 13px;
        }
        
        tr:nth-child(even) td {
            background-color: #f9fafe;
        }
        
        tr:hover td {
            background-color: #f0f3ff;
        }
        
        .status-rejected {
            background-color: #ffebee !important;
        }
        
        .status-conditional {
            background-color: #fff3e0 !important;
        }
        
        .status-accepted {
            background-color: #e8f5e9 !important;
        }
        
        .status-cell {
            width: 120px;
        }
        
        .input-small {
            width: 80px;
        }
        
        .input-medium {
            width: 120px;
        }
        
        .input-large {
            width: 150px;
        }
        
        /* بخش وضعیت */
        .status-options {
            display: flex;
            flex-direction: column;
            gap: 8px;
            align-items: flex-start;
        }
        
        .status-option {
            display: flex;
            align-items: center;
            gap: 6px;
            cursor: pointer;
        }
        
        .status-option input[type="radio"] {
            width: 16px;
            height: 16px;
            cursor: pointer;
        }
        
        .status-rejected-radio {
            accent-color: #f44336;
        }
        
        .status-conditional-radio {
            accent-color: #ff9800;
        }
        
        .status-accepted-radio {
            accent-color: #4caf50;
        }
        
        /* بخش علت مردودی و پارامترها */
        .rejection-reason, .conditional-info {
            margin-top: 10px;
            width: 100%;
        }
        
        /* دکمه‌ها */
        .buttons {
            display: flex;
            gap: 12px;
            margin-top: 30px;
            justify-content: center;
            flex-wrap: wrap;
        }
        
        button {
            padding: 12px 25px;
            border: none;
            border-radius: 6px;
            font-size: 15px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            min-width: 150px;
            box-shadow: 0 3px 8px rgba(0, 0, 0, 0.1);
        }
        
        .btn-save {
            background: linear-gradient(to right, #4caf50, #388e3c);
            color: white;
        }
        
        .btn-save:hover {
            background: linear-gradient(to right, #43a047, #2e7d32);
            transform: translateY(-2px);
            box-shadow: 0 5px 12px rgba(76, 175, 80, 0.25);
        }
        
        .btn-print {
            background: linear-gradient(to right, #2196f3, #1565c0);
            color: white;
        }
        
        .btn-print:hover {
            background: linear-gradient(to right, #1976d2, #0d47a1);
            transform: translateY(-2px);
            box-shadow: 0 5px 12px rgba(33, 150, 243, 0.25);
        }
        
        .btn-reset {
            background: linear-gradient(to right, #f44336, #d32f2f);
            color: white;
        }
        
        .btn-reset:hover {
            background: linear-gradient(to right, #e53935, #c62828);
            transform: translateY(-2px);
            box-shadow: 0 5px 12px rgba(244, 67, 54, 0.25);
        }
        
        .btn-export {
            background: linear-gradient(to right, #ff9800, #f57c00);
            color: white;
        }
        
        .btn-export:hover {
            background: linear-gradient(to right, #fb8c00, #ef6c00);
            transform: translateY(-2px);
            box-shadow: 0 5px 12px rgba(255, 152, 0, 0.25);
        }
        
        .btn-excel {
            background: linear-gradient(to right, #217346, #1b5e3a);
            color: white;
        }
        
        .btn-excel:hover {
            background: linear-gradient(to right, #1b5e3a, #14532d);
            transform: translateY(-2px);
            box-shadow: 0 5px 12px rgba(33, 115, 70, 0.25);
        }
        
        /* توضیحات پایین */
        .status-explanations {
            margin-top: 30px;
            padding: 20px;
            background: #f8f9fa;
            border-radius: 8px;
            border-right: 4px solid #5c6bc0;
        }
        
        .explanation-title {
            color: #1a237e;
            font-weight: bold;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .explanation-title i {
            color: #ff5252;
        }
        
        .explanations {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 15px;
        }
        
        .explanation-item {
            flex: 1;
            min-width: 300px;
            padding: 15px;
            border-radius: 6px;
        }
        
        .rejected-explanation {
            background: #ffebee;
            border: 1px solid #ffcdd2;
        }
        
        .conditional-explanation {
            background: #fff3e0;
            border: 1px solid #ffe0b2;
        }
        
        .accepted-explanation {
            background: #e8f5e9;
            border: 1px solid #c8e6c9;
        }
        
        .explanation-item h4 {
            color: #333;
            margin-bottom: 8px;
            font-size: 16px;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .explanation-item p {
            color: #555;
            font-size: 14px;
            line-height: 1.6;
        }
        
        /* فوتر */
        .footer {
            margin-top: 30px;
            text-align: center;
            color: #555;
            font-size: 13px;
            padding-top: 20px;
            border-top: 1px solid #eee;
            background-color: #f8f9ff;
            padding: 20px;
            border-radius: 0 0 12px 12px;
            line-height: 1.8;
        }
        
        .company-details {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 15px;
            font-size: 14px;
        }
        
        .detail-item {
            display: flex;
            align-items: center;
            gap: 7px;
            color: #444;
        }
        
        /* چاپ */
        @media print {
            .company-header {
                background: #1a237e !important;
                -webkit-print-color-adjust: exact;
                color-adjust: exact;
            }
            
            .buttons, .add-row-btn {
                display: none !important;
            }
            
            body {
                background-color: white;
                padding: 5px;
            }
            
            .container {
                box-shadow: none;
                border: 1px solid #ccc;
            }
            
            th {
                background: #3f51b5 !important;
                -webkit-print-color-adjust: exact;
                color-adjust: exact;
            }
            
            .status-explanations {
                page-break-inside: avoid;
            }
        }
        
        /* موبایل */
        @media (max-width: 768px) {
            .form-container {
                padding: 20px 15px;
            }
            
            .company-header {
                padding: 20px 15px;
            }
            
            .company-name {
                font-size: 24px;
            }
            
            .company-subtitle {
                font-size: 16px;
            }
            
            .header-section {
                flex-direction: column;
                align-items: stretch;
            }
            
            .center-info {
                flex-direction: column;
                gap: 15px;
            }
            
            .center-info-item {
                min-width: 100%;
            }
            
            th, td {
                padding: 10px 6px;
                font-size: 12px;
            }
            
            button {
                min-width: 130px;
                padding: 10px 18px;
                font-size: 14px;
            }
            
            .buttons {
                gap: 10px;
            }
            
            .explanations {
                flex-direction: column;
            }
            
            .explanation-item {
                min-width: 100%;
            }
        }
        
        /* دکمه جدید ردیف */
        .add-row-btn {
            background: linear-gradient(to right, #9c27b0, #7b1fa2);
            color: white;
            padding: 10px 18px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            margin-top: 12px;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: all 0.3s;
            font-size: 14px;
        }
        
        .add-row-btn:hover {
            background: linear-gradient(to right, #8e24aa, #6a1b9a);
            transform: translateY(-2px);
        }
        
        .delete-row-btn {
            background: none;
            border: none;
            color: #f44336;
            cursor: pointer;
            font-size: 16px;
            width: 28px;
            height: 28px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 4px;
            transition: all 0.2s;
        }
        
        .delete-row-btn:hover {
            background-color: rgba(244, 67, 54, 0.1);
        }
        
        .english-font {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        .hidden {
            display: none;
        }
        
        /* استایل برای ریزالت اکسل */
        .excel-results {
            margin-top: 20px;
            padding: 15px;
            background: #f8f9fa;
            border-radius: 8px;
            border: 1px solid #dee2e6;
        }
        
        .results-title {
            color: #1a237e;
            font-weight: bold;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .results-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-top: 15px;
        }
        
        .result-item {
            background: white;
            padding: 15px;
            border-radius: 6px;
            border-left: 4px solid #5c6bc0;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
        }
        
        .result-item.rejected {
            border-left-color: #f44336;
        }
        
        .result-item.conditional {
            border-left-color: #ff9800;
        }
        
        .result-item.accepted {
            border-left-color: #4caf50;
        }
        
        .result-value {
            font-size: 24px;
            font-weight: bold;
            text-align: center;
            margin: 5px 0;
        }
        
        .result-label {
            font-size: 14px;
            text-align: center;
            color: #666;
        }
        
        .excel-preview {
            max-height: 300px;
            overflow-y: auto;
            margin-top: 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            background: white;
            padding: 10px;
            font-family: monospace;
            font-size: 12px;
            white-space: pre;
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>
    <div class="container">
        <!-- هدر شرکت آترا طب قومس -->
        <div class="company-header">
            <h1 class="company-name">شرکت آترا طب قومس</h1>
            <div class="company-subtitle">سیستم کنترل کیفی تجهیزات پزشکی و آزمایشگاهی</div>
            
            <div class="company-info">
                <div class="info-item">
                    <i class="fas fa-map-marker-alt"></i>
                    <span>سمنان - بلوار 17 شهریور، جنب دانشکده دندانپزشکی، مرکز رشد فناوری سلامت</span>
                </div>
                <div class="info-item">
                    <i class="fas fa-phone"></i>
                    <span>0910-032-1022</span>
                </div>
                <div class="info-item">
                    <i class="fas fa-envelope"></i>
                    <span>atra.teb@yahoo.com</span>
                </div>
            </div>
        </div>
        
        <!-- بخش اصلی فرم -->
        <div class="form-container">
            <h2 class="form-title">فرم کنترل کیفی تجهیزات پزشکی</h2>
            
            <div class="header-section">
                <div class="center-info">
                    <div class="center-info-item">
                        <label><i class="fas fa-hospital"></i> نام مرکز درمانی:</label>
                        <input type="text" id="medical-center" placeholder="بیمارستان امام خمینی / درمانگاه تخصصی / ..." value="بیمارستان امام خمینی">
                    </div>
                    <div class="center-info-item">
                        <label><i class="fas fa-calendar-alt"></i> تاریخ بازرسی:</label>
                        <input type="text" id="inspection-date" placeholder="1403/05/15" value="">
                    </div>
                    <div class="center-info-item">
                        <label><i class="fas fa-clipboard-check"></i> شماره گزارش:</label>
                        <input type="text" id="report-number" placeholder="QC-MED-1403-001" value="QC-MED-1403-001">
                    </div>
                </div>
            </div>
            
            <div class="table-container">
                <table id="qc-table">
                    <thead>
                        <tr>
                            <th>ردیف</th>
                            <th>شماره</th>
                            <th>نام دستگاه</th>
                            <th>سازنده</th>
                            <th>مدل</th>
                            <th>سریال</th>
                            <th>شماره اموال</th>
                            <th>محل استقرار</th>
                            <th>وضعیت</th>
                            <th>علت مردودی</th>
                            <th>پارامتر غیرفعال</th>
                            <th>شرایط استفاده (مشروط)</th>
                            <th>عملیات</th>
                        </tr>
                    </thead>
                    <tbody id="table-body">
                        <!-- ردیف‌ها به صورت پویا اضافه می‌شوند -->
                    </tbody>
                </table>
                <button type="button" class="add-row-btn" onclick="addNewRow()">
                    <i class="fas fa-plus-circle"></i> افزودن دستگاه جدید
                </button>
            </div>
            
            <!-- بخش ریزالت اکسل -->
            <div class="excel-results hidden" id="excel-results">
                <div class="results-title">
                    <i class="fas fa-chart-bar"></i>
                    <span>ریزالت گزارش کنترل کیفی</span>
                </div>
                <div class="results-grid" id="results-grid">
                    <!-- نتایج به صورت پویا اضافه می‌شوند -->
                </div>
                <div class="excel-preview" id="excel-preview">
                    <!-- پیش‌نمایش اکسل -->
                </div>
            </div>
            
            <!-- توضیح وضعیت‌ها -->
            <div class="status-explanations">
                <div class="explanation-title">
                    <i class="fas fa-info-circle"></i>
                    <span>توضیح وضعیت‌های کنترل کیفی:</span>
                </div>
                <div class="explanations">
                    <div class="explanation-item rejected-explanation">
                        <h4><i class="fas fa-times-circle" style="color: #f44336;"></i> مردودی (Rejected)</h4>
                        <p>دستگاه دارای نقص فنی جدی است، استفاده از آن خطرناک بوده و باید از سرویس خارج شود. نیاز به تعمیر اساسی یا تعویض دارد.</p>
                    </div>
                    <div class="explanation-item conditional-explanation">
                        <h4><i class="fas fa-exclamation-triangle" style="color: #ff9800;"></i> مشروط (Conditional)</h4>
                        <p>دستگاه دارای محدودیت در عملکرد است. برخی پارامترها غیرفعال هستند اما در شرایط خاص و با رعایت نکات ایمنی قابل استفاده است.</p>
                    </div>
                    <div class="explanation-item accepted-explanation">
                        <h4><i class="fas fa-check-circle" style="color: #4caf50;"></i> قبول (Accepted)</h4>
                        <p>دستگاه در وضعیت مطلوب قرار دارد، تمام پارامترها فعال بوده و مطابق با استانداردهای کنترل کیفیت می‌باشد.</p>
                    </div>
                </div>
            </div>
            
            <div class="buttons">
                <button class="btn-save" onclick="saveData()">
                    <i class="fas fa-save"></i> ذخیره گزارش
                </button>
                <button class="btn-print" onclick="window.print()">
                    <i class="fas fa-print"></i> چاپ فرم
                </button>
                <button class="btn-export" onclick="exportToExcel()">
                    <i class="fas fa-file-excel"></i> خروجی Excel
                </button>
                <button class="btn-excel" onclick="showExcelResults()">
                    <i class="fas fa-chart-pie"></i> ریزالت Excel
                </button>
                <button class="btn-reset" onclick="resetForm()">
                    <i class="fas fa-redo"></i> فرم جدید
                </button>
            </div>
        </div>
        
        <!-- فوتر -->
        <div class="footer">
            <div class="company-details">
                <div class="detail-item">
                    <i class="fas fa-map-marker-alt"></i>
                    <span>آدرس: سمنان - بلوار 17 شهریور، جنب دانشکده دندانپزشکی، مرکز رشد فناوری سلامت</span>
                </div>
                <div class="detail-item">
                    <i class="fas fa-phone"></i>
                    <span>تلفن: 0910-032-1022</span>
                </div>
                <div class="detail-item">
                    <i class="fas fa-envelope"></i>
                    <span>ایمیل: atra.teb@yahoo.com</span>
                </div>
            </div>
            <div style="margin-top: 10px; color: #666; font-size: 12.5px;">
                این فرم جهت کنترل دوره‌ای کیفی تجهیزات پزشکی طراحی شده است. گزارش‌های مردودی باید ظرف 48 ساعت به واحد فنی ارجاع شوند.
            </div>
        </div>
    </div>

    <script>
        // داده‌های اولیه
        let rowCounter = 1;
        let deviceCounter = 1;
        
        // محل‌های استقرار پیش‌فرض
        const locations = [
            "ICU", "CCU", "اتاق عمل", "اورژانس", "بخش داخلی", 
            "بخش جراحی", "بخش اطفال", "بخش زنان", "بخش ارتوپدی",
            "آزمایشگاه", "رادیولوژی", "سونوگرافی", "فیزیوتراپی",
            "اتاق استریل", "انبار تجهیزات", "کارگاه تعمیرات"
        ];
        
        // سازندگان پیش‌فرض
        const manufacturers = [
            "Philips", "GE Healthcare", "Siemens Healthineers", "Mindray",
            "Drager", "Hamilton Medical", "Getinge", "Maquet",
            "Fresenius", "B. Braun", "Baxter", "Medtronic",
            "Stryker", "Hill-Rom", "Mortara", "Schiller",
            "Zoll", "Nihon Kohden", "Fukuda Denshi", "国产 (داخلی)"
        ];
        
        // نام دستگاه‌های پیش‌فرض
        const deviceNames = [
            "دفیبریلاتور", "مانیتور علائم حیاتی", "پمپ انفوزیون", 
            "ونتیلاتور", "الکتروکاردیوگراف", "سانتریفیوژ", 
            "اتوکلاو", "آنالایزر گاز خون", "اکسیژن ساز",
            "تخت بیمارستانی", "لامپ جراحی", "ساکشن",
            "دستگاه سونوگرافی", "دستگاه رادیولوژی", "دستگاه MRI",
            "دستگاه CT Scan", "دستگاه دیالیز", "دستگاه اندوسکوپی",
            "دستگاه کولونوسکوپی", "دستگاه افتالموسکوپی"
        ];
        
        // تابع برای ایجاد یک ردیف جدید
        function createRow(rowNum) {
            return `
                <tr id="row-${rowNum}">
                    <td class="english-font">${rowNum}</td>
                    <td>
                        <input type="text" class="device-id english-font" placeholder="D-${deviceCounter}" 
                               value="D-${deviceCounter++}" style="width: 70px; text-align: center;">
                    </td>
                    <td>
                        <input type="text" class="device-name" placeholder="نام دستگاه" data-field="name" list="device-names">
                    </td>
                    <td>
                        <input type="text" class="manufacturer" placeholder="سازنده" data-field="manufacturer" list="manufacturers">
                    </td>
                    <td>
                        <input type="text" class="model" placeholder="مدل" data-field="model">
                    </td>
                    <td>
                        <input type="text" class="serial english-font" placeholder="SN-xxxxxx" data-field="serial">
                    </td>
                    <td>
                        <input type="text" class="asset-number english-font" placeholder="AM-xxx" data-field="asset">
                    </td>
                    <td>
                        <select class="location" data-field="location" style="width: 120px;">
                            <option value="">انتخاب محل</option>
                            ${locations.map(loc => `<option value="${loc}">${loc}</option>`).join('')}
                        </select>
                    </td>
                    <td class="status-cell">
                        <div class="status-options">
                            <div class="status-option">
                                <input type="radio" name="status-${rowNum}" value="rejected" class="status-rejected-radio" 
                                       onchange="updateRowStatus(${rowNum}, 'rejected')">
                                <span style="color: #f44336; font-weight: bold;">مردودی</span>
                            </div>
                            <div class="status-option">
                                <input type="radio" name="status-${rowNum}" value="conditional" class="status-conditional-radio" 
                                       onchange="updateRowStatus(${rowNum}, 'conditional')">
                                <span style="color: #ff9800; font-weight: bold;">مشروط</span>
                            </div>
                            <div class="status-option">
                                <input type="radio" name="status-${rowNum}" value="accepted" class="status-accepted-radio" 
                                       onchange="updateRowStatus(${rowNum}, 'accepted')" checked>
                                <span style="color: #4caf50; font-weight: bold;">قبول</span>
                            </div>
                        </div>
                    </td>
                    <td>
                        <div class="rejection-reason hidden">
                            <textarea class="rejection-reason-text" placeholder="علت مردودی" 
                                      rows="2" style="width: 100%; font-size: 11px;"></textarea>
                        </div>
                    </td>
                    <td>
                        <div class="conditional-info hidden">
                            <textarea class="disabled-params" placeholder="پارامترهای غیرفعال" 
                                      rows="2" style="width: 100%; font-size: 11px;"></textarea>
                        </div>
                    </td>
                    <td>
                        <div class="conditional-info hidden">
                            <textarea class="usage-conditions" placeholder="شرایط استفاده" 
                                      rows="2" style="width: 100%; font-size: 11px;"></textarea>
                        </div>
                    </td>
                    <td>
                        <button type="button" class="delete-row-btn" onclick="deleteRow(${rowNum})" title="حذف ردیف">
                            <i class="fas fa-trash"></i>
                        </button>
                    </td>
                </tr>
            `;
        }
        
        // تابع به‌روزرسانی وضعیت ردیف
        function updateRowStatus(rowNum, status) {
            const row = document.getElementById(`row-${rowNum}`);
            if (!row) return;
            
            // حذف کلاس‌های وضعیت قبلی
            row.classList.remove('status-rejected', 'status-conditional', 'status-accepted');
            
            // اضافه کردن کلاس جدید
            row.classList.add(`status-${status}`);
            
            // نمایش/پنهان کردن فیلدهای مرتبط
            const rejectionReasonDiv = row.querySelector('.rejection-reason');
            const conditionalInfoDivs = row.querySelectorAll('.conditional-info');
            
            switch(status) {
                case 'rejected':
                    rejectionReasonDiv.classList.remove('hidden');
                    conditionalInfoDivs.forEach(div => div.classList.remove('hidden'));
                    break;
                case 'conditional':
                    rejectionReasonDiv.classList.add('hidden');
                    conditionalInfoDivs.forEach(div => div.classList.remove('hidden'));
                    break;
                case 'accepted':
                    rejectionReasonDiv.classList.add('hidden');
                    conditionalInfoDivs.forEach(div => div.classList.add('hidden'));
                    break;
            }
            
            // به‌روزرسانی ریزالت اگر نمایش داده می‌شود
            if (!document.getElementById('excel-results').classList.contains('hidden')) {
                showExcelResults();
            }
        }
        
        // تابع افزودن ردیف جدید
        function addNewRow() {
            rowCounter++;
            const tableBody = document.getElementById('table-body');
            tableBody.innerHTML += createRow(rowCounter);
        }
        
        // تابع حذف ردیف
        function deleteRow(rowNum) {
            if (rowCounter > 1) {
                const row = document.getElementById(`row-${rowNum}`);
                if (row) {
                    row.remove();
                    // به روز رسانی شماره ردیف‌ها
                    updateRowNumbers();
                    // به‌روزرسانی ریزالت
                    if (!document.getElementById('excel-results').classList.contains('hidden')) {
                        showExcelResults();
                    }
                }
            } else {
                alert("حداقل باید یک ردیف در جدول وجود داشته باشد.");
            }
        }
        
        // تابع به روز رسانی شماره ردیف‌ها
        function updateRowNumbers() {
            const rows = document.querySelectorAll('#table-body tr');
            rowCounter = rows.length;
            
            rows.forEach((row, index) => {
                const rowNum = index + 1;
                row.id = `row-${rowNum}`;
                row.cells[0].textContent = rowNum;
                
                // به روز رسانی تابع حذف
                const deleteBtn = row.querySelector('.delete-row-btn');
                if (deleteBtn) {
                    deleteBtn.setAttribute('onclick', `deleteRow(${rowNum})`);
                }
            });
        }
        
        // تابع نمایش ریزالت اکسل
        function showExcelResults() {
            const rows = document.querySelectorAll('#table-body tr');
            
            if (rows.length === 0) {
                alert('هیچ داده‌ای برای نمایش وجود ندارد.');
                return;
            }
            
            // محاسبه آمار
            let rejectedCount = 0;
            let conditionalCount = 0;
            let acceptedCount = 0;
            const locationStats = {};
            const manufacturerStats = {};
            
            rows.forEach(row => {
                const status = row.querySelector('.status-rejected-radio').checked ? 'rejected' : 
                              row.querySelector('.status-conditional-radio').checked ? 'conditional' : 'accepted';
                
                if (status === 'rejected') rejectedCount++;
                else if (status === 'conditional') conditionalCount++;
                else acceptedCount++;
                
                // آمار بر اساس محل استقرار
                const location = row.querySelector('.location').value;
                if (location) {
                    if (!locationStats[location]) locationStats[location] = { total: 0, rejected: 0, conditional: 0, accepted: 0 };
                    locationStats[location].total++;
                    locationStats[location][status]++;
                }
                
                // آمار بر اساس سازنده
                const manufacturer = row.querySelector('.manufacturer').value;
                if (manufacturer) {
                    if (!manufacturerStats[manufacturer]) manufacturerStats[manufacturer] = { total: 0, rejected: 0, conditional: 0, accepted: 0 };
                    manufacturerStats[manufacturer].total++;
                    manufacturerStats[manufacturer][status]++;
                }
            });
            
            const totalCount = rows.length;
            
            // ایجاد HTML برای ریزالت
            const resultsHTML = `
                <div class="result-item">
                    <div class="result-value" style="color: #1a237e;">${totalCount}</div>
                    <div class="result-label">تعداد کل دستگاه‌ها</div>
                </div>
                <div class="result-item rejected">
                    <div class="result-value" style="color: #f44336;">${rejectedCount}</div>
                    <div class="result-label">دستگاه مردود</div>
                    <div style="font-size: 12px; color: #777; text-align: center; margin-top: 5px;">
                        ${totalCount > 0 ? Math.round((rejectedCount / totalCount) * 100) : 0}%
                    </div>
                </div>
                <div class="result-item conditional">
                    <div class="result-value" style="color: #ff9800;">${conditionalCount}</div>
                    <div class="result-label">دستگاه مشروط</div>
                    <div style="font-size: 12px; color: #777; text-align: center; margin-top: 5px;">
                        ${totalCount > 0 ? Math.round((conditionalCount / totalCount) * 100) : 0}%
                    </div>
                </div>
                <div class="result-item accepted">
                    <div class="result-value" style="color: #4caf50;">${acceptedCount}</div>
                    <div class="result-label">دستگاه قابل قبول</div>
                    <div style="font-size: 12px; color: #777; text-align: center; margin-top: 5px;">
                        ${totalCount > 0 ? Math.round((acceptedCount / totalCount) * 100) : 0}%
                    </div>
                </div>
            `;
            
            // ایجاد HTML برای آمار محل‌های استقرار
            let locationHTML = '';
            Object.keys(locationStats).slice(0, 5).forEach(location => {
                const stats = locationStats[location];
                locationHTML += `
                    <div class="result-item">
                        <div style="font-size: 14px; font-weight: bold; margin-bottom: 5px;">${location}</div>
                        <div style="display: flex; justify-content: space-between; font-size: 12px;">
                            <span>کل: ${stats.total}</span>
                            <span style="color: #f44336;">م: ${stats.rejected}</span>
                            <span style="color: #ff9800;">ش: ${stats.conditional}</span>
                            <span style="color: #4caf50;">ق: ${stats.accepted}</span>
                        </div>
                    </div>
                `;
            });
            
            // ایجاد پیش‌نمایش داده‌های اکسل
            let excelPreview = "ردیف\tشماره\tنام دستگاه\tسازنده\tمدل\tسریال\tشماره اموال\tمحل استقرار\tوضعیت\tعلت مردودی\tپارامترهای غیرفعال\tشرایط استفاده\n";
            
            rows.forEach((row, index) => {
                const rowNum = index + 1;
                const deviceId = row.querySelector('.device-id').value || '';
                const deviceName = row.querySelector('.device-name').value || '';
                const manufacturer = row.querySelector('.manufacturer').value || '';
                const model = row.querySelector('.model').value || '';
                const serial = row.querySelector('.serial').value || '';
                const asset = row.querySelector('.asset-number').value || '';
                const location = row.querySelector('.location').value || '';
                
                const status = row.querySelector('.status-rejected-radio').checked ? 'مردودی' : 
                              row.querySelector('.status-conditional-radio').checked ? 'مشروط' : 'قبول';
                
                const rejectionReason = (row.querySelector('.rejection-reason-text')?.value || '').replace(/\n/g, ' ');
                const disabledParams = (row.querySelector('.disabled-params')?.value || '').replace(/\n/g, ' ');
                const usageConditions = (row.querySelector('.usage-conditions')?.value || '').replace(/\n/g, ' ');
                
                excelPreview += `${rowNum}\t${deviceId}\t${deviceName}\t${manufacturer}\t${model}\t${serial}\t${asset}\t${location}\t${status}\t${rejectionReason}\t${disabledParams}\t${usageConditions}\n`;
            });
            
            // افزودن آمار به پیش‌نمایش
            excelPreview += `\n\nآمار کلی:\n`;
            excelPreview += `تعداد کل دستگاه‌ها:\t${totalCount}\n`;
            excelPreview += `دستگاه مردود:\t${rejectedCount}\t(${totalCount > 0 ? Math.round((rejectedCount / totalCount) * 100) : 0}%)\n`;
            excelPreview += `دستگاه مشروط:\t${conditionalCount}\t(${totalCount > 0 ? Math.round((conditionalCount / totalCount) * 100) : 0}%)\n`;
            excelPreview += `دستگاه قابل قبول:\t${acceptedCount}\t(${totalCount > 0 ? Math.round((acceptedCount / totalCount) * 100) : 0}%)\n`;
            
            // نمایش نتایج
            document.getElementById('results-grid').innerHTML = resultsHTML + locationHTML;
            document.getElementById('excel-preview').textContent = excelPreview;
            document.getElementById('excel-results').classList.remove('hidden');
            
            // اسکرول به بخش ریزالت
            document.getElementById('excel-results').scrollIntoView({ behavior: 'smooth' });
        }
        
        // تابع ذخیره اطلاعات
        function saveData() {
            const medicalCenter = document.getElementById('medical-center').value || 'نامشخص';
            const inspectionDate = document.getElementById('inspection-date').value || 'تاریخ نامشخص';
            const reportNumber = document.getElementById('report-number').value || 'شماره نامشخص';
            
            const data = {
                company: "شرکت آترا طب قومس",
                medicalCenter: medicalCenter,
                inspectionDate: inspectionDate,
                reportNumber: reportNumber,
                devices: [],
                summary: {
                    total: 0,
                    rejected: 0,
                    conditional: 0,
                    accepted: 0
                }
            };
            
            const rows = document.querySelectorAll('#table-body tr');
            rows.forEach(row => {
                const device = {
                    id: row.querySelector('.device-id').value,
                    name: row.querySelector('.device-name').value,
                    manufacturer: row.querySelector('.manufacturer').value,
                    model: row.querySelector('.model').value,
                    serial: row.querySelector('.serial').value,
                    asset: row.querySelector('.asset-number').value,
                    location: row.querySelector('.location').value,
                    status: row.querySelector('.status-rejected-radio').checked ? 'rejected' : 
                            row.querySelector('.status-conditional-radio').checked ? 'conditional' : 'accepted',
                    rejectionReason: row.querySelector('.rejection-reason-text')?.value || '',
                    disabledParams: row.querySelector('.disabled-params')?.value || '',
                    usageConditions: row.querySelector('.usage-conditions')?.value || ''
                };
                
                data.devices.push(device);
                
                // آمار
                data.summary.total++;
                if (device.status === 'rejected') data.summary.rejected++;
                else if (device.status === 'conditional') data.summary.conditional++;
                else data.summary.accepted++;
            });
            
            // ذخیره در localStorage
            localStorage.setItem('atratab_medical_qc_v2', JSON.stringify(data));
            
            // نمایش پیام موفقیت با خلاصه
            const summaryText = `مرکز: ${medicalCenter}\nتعداد کل: ${data.summary.total} | مردودی: ${data.summary.rejected} | مشروط: ${data.summary.conditional} | قبول: ${data.summary.accepted}`;
            
            alert(`✅ گزارش کنترل کیفی با شماره ${reportNumber} ذخیره شد.\n\n${summaryText}\n\nگزارش‌های مردودی باید ظرف 48 ساعت به واحد فنی ارجاع شوند.`);
            
            // نمایش در کنسول
            console.log('📋 گزارش کنترل کیفی تجهیزات پزشکی:', data);
        }
        
        // تابع خروجی به Excel
        function exportToExcel() {
            const medicalCenter = document.getElementById('medical-center').value || 'نامشخص';
            const inspectionDate = document.getElementById('inspection-date').value || 'تاریخ نامشخص';
            const reportNumber = document.getElementById('report-number').value || 'شماره نامشخص';
            
            // ایجاد یک رشته CSV
            let csv = 'شرکت آترا طب قومس - گزارش کنترل کیفی تجهیزات پزشکی\n';
            csv += 'آدرس: سمنان - بلوار 17 شهریور، جنب دانشکده دندانپزشکی، مرکز رشد فناوری سلامت\n';
            csv += `تلفن: 0910-032-1022 | ایمیل: atra.teb@yahoo.com\n\n`;
            
            csv += `مرکز درمانی: ${medicalCenter}\n`;
            csv += `تاریخ بازرسی: ${inspectionDate}\n`;
            csv += `شماره گزارش: ${reportNumber}\n\n`;
            
            csv += 'ردیف,شماره,نام دستگاه,سازنده,مدل,سریال,شماره اموال,محل استقرار,وضعیت,علت مردودی,پارامترهای غیرفعال,شرایط استفاده\n';
            
            const rows = document.querySelectorAll('#table-body tr');
            rows.forEach((row, index) => {
                const rowNum = index + 1;
                const deviceId = row.querySelector('.device-id').value || '';
                const deviceName = row.querySelector('.device-name').value || '';
                const manufacturer = row.querySelector('.manufacturer').value || '';
                const model = row.querySelector('.model').value || '';
                const serial = row.querySelector('.serial').value || '';
                const asset = row.querySelector('.asset-number').value || '';
                const location = row.querySelector('.location').value || '';
                
                const status = row.querySelector('.status-rejected-radio').checked ? 'مردودی' : 
                              row.querySelector('.status-conditional-radio').checked ? 'مشروط' : 'قبول';
                
                const rejectionReason = (row.querySelector('.rejection-reason-text')?.value || '').replace(/"/g, '""');
                const disabledParams = (row.querySelector('.disabled-params')?.value || '').replace(/"/g, '""');
                const usageConditions = (row.querySelector('.usage-conditions')?.value || '').replace(/"/g, '""');
                
                csv += `${rowNum},${deviceId},"${deviceName}","${manufacturer}","${model}",${serial},${asset},"${location}",${status},"${rejectionReason}","${disabledParams}","${usageConditions}"\n`;
            });
            
            // خلاصه گزارش
            const rejectedCount = Array.from(rows).filter(r => r.querySelector('.status-rejected-radio').checked).length;
            const conditionalCount = Array.from(rows).filter(r => r.querySelector('.status-conditional-radio').checked).length;
            const acceptedCount = Array.from(rows).filter(r => r.querySelector('.status-accepted-radio').checked).length;
            const totalCount = rows.length;
            
            csv += `\nخلاصه گزارش:\n`;
            csv += `تعداد کل دستگاه‌ها:,${totalCount}\n`;
            csv += `دستگاه مردود:,${rejectedCount}\n`;
            csv += `دستگاه مشروط:,${conditionalCount}\n`;
            csv += `دستگاه قبول:,${acceptedCount}\n\n`;
            csv += `درصد مردودی:,${totalCount > 0 ? Math.round((rejectedCount / totalCount) * 100) : 0}%\n`;
            csv += `درصد مشروط:,${totalCount > 0 ? Math.round((conditionalCount / totalCount) * 100) : 0}%\n`;
            csv += `درصد قبول:,${totalCount > 0 ? Math.round((acceptedCount / totalCount) * 100) : 0}%\n\n`;
            csv += `مرکز درمانی: ${medicalCenter}\n`;
            csv += `تاریخ صدور گزارش: ${inspectionDate}\n`;
            csv += `امضای مسئول کنترل کیفی: _________________\n`;
            csv += `مهر و تأیید: _________________`;
            
            // ایجاد فایل و دانلود
            const blob = new Blob(["\ufeff" + csv], { type: 'text/csv;charset=utf-8;' });
            const link = document.createElement('a');
            const url = URL.createObjectURL(blob);
            
            link.href = url;
            link.download = `QC_Medical_${reportNumber}_${inspectionDate.replace(/\//g, '-')}.csv`;
            link.click();
            
            URL.revokeObjectURL(url);
            
            alert('✅ فایل خروجی با فرمت Excel (CSV) آماده شد.');
        }
        
        // تابع پاک کردن فرم
        function resetForm() {
            if (confirm('آیا مطمئن هستید که می‌خواهید همه اطلاعات فرم را پاک کنید؟')) {
                document.getElementById('medical-center').value = 'بیمارستان امام خمینی';
                document.getElementById('report-number').value = 'QC-MED-1403-001';
                
                // پاک کردن ردیف‌ها و ایجاد مجدد
                const tableBody = document.getElementById('table-body');
                tableBody.innerHTML = '';
                
                // مخفی کردن ریزالت
                document.getElementById('excel-results').classList.add('hidden');
                
                // ایجاد 3 ردیف اولیه
                for (let i = 1; i <= 3; i++) {
                    tableBody.innerHTML += createRow(i);
                }
                
                rowCounter = 3;
                deviceCounter = 1;
                
                alert('✅ فرم با موفقیت پاک و به حالت اولیه بازگردانده شد.');
            }
        }
        
        // تابع تبدیل تاریخ میلادی به شمسی (ساده شده)
        function getCurrentPersianDate() {
            const now = new Date();
            const options = { year: 'numeric', month: '2-digit', day: '2-digit' };
            return now.toLocaleDateString('fa-IR', options);
        }
        
        // تابع بارگذاری داده‌های نمونه (برای نمایش)
        function loadSampleData() {
            const sampleDevices = [
                {
                    id: 'D-101',
                    name: 'دفیبریلاتور',
                    manufacturer: 'Philips',
                    model: 'HeartStart XL',
                    serial: 'PH-789012',
                    asset: 'AM-101',
                    location: 'اورژانس',
                    status: 'accepted'
                },
                {
                    id: 'D-102',
                    name: 'مانیتور علائم حیاتی',
                    manufacturer: 'Mindray',
                    model: 'BeneVision N12',
                    serial: 'MR-345678',
                    asset: 'AM-102',
                    location: 'ICU',
                    status: 'conditional',
                    disabledParams: 'آلارم فشار خون غیرفعال',
                    usageConditions: 'استفاده همراه با دستگاه فشارسنج جداگانه'
                },
                {
                    id: 'D-103',
                    name: 'پمپ انفوزیون',
                    manufacturer: 'B. Braun',
                    model: 'Infusomat Space',
                    serial: 'BB-901234',
                    asset: 'AM-103',
                    location: 'بخش داخلی',
                    status: 'rejected',
                    rejectionReason: 'خطای کالیبراسیون دوز، ریزش مایع',
                    disabledParams: 'تمام پارامترها',
                    usageConditions: 'غیرقابل استفاده'
                },
                {
                    id: 'D-104',
                    name: 'ونتیلاتور',
                    manufacturer: 'Hamilton Medical',
                    model: 'C1',
                    serial: 'HM-567890',
                    asset: 'AM-104',
                    location: 'CCU',
                    status: 'accepted'
                },
                {
                    id: 'D-105',
                    name: 'الکتروکاردیوگراف',
                    manufacturer: 'Schiller',
                    model: 'AT-102',
                    serial: 'SC-123456',
                    asset: 'AM-105',
                    location: 'بخش قلب',
                    status: 'conditional',
                    disabledParams: 'کانال 3 غیرفعال',
                    usageConditions: 'استفاده فقط با 6 لید'
                }
            ];
            
            // حذف ردیف‌های فعلی
            const tableBody = document.getElementById('table-body');
            tableBody.innerHTML = '';
            
            // ایجاد ردیف‌های نمونه
            sampleDevices.forEach((device, index) => {
                rowCounter = index + 1;
                tableBody.innerHTML += createRow(rowCounter);
                
                // پر کردن داده‌ها
                const row = document.getElementById(`row-${rowCounter}`);
                row.querySelector('.device-id').value = device.id;
                row.querySelector('.device-name').value = device.name;
                row.querySelector('.manufacturer').value = device.manufacturer;
                row.querySelector('.model').value = device.model;
                row.querySelector('.serial').value = device.serial;
                row.querySelector('.asset-number').value = device.asset;
                row.querySelector('.location').value = device.location;
                
                // تنظیم وضعیت
                if (device.status === 'rejected') {
                    row.querySelector('.status-rejected-radio').checked = true;
                    updateRowStatus(rowCounter, 'rejected');
                    row.querySelector('.rejection-reason-text').value = device.rejectionReason || '';
                    row.querySelector('.disabled-params').value = device.disabledParams || '';
                    row.querySelector('.usage-conditions').value = device.usageConditions || '';
                } else if (device.status === 'conditional') {
                    row.querySelector('.status-conditional-radio').checked = true;
                    updateRowStatus(rowCounter, 'conditional');
                    row.querySelector('.disabled-params').value = device.disabledParams || '';
                    row.querySelector('.usage-conditions').value = device.usageConditions || '';
                } else {
                    row.querySelector('.status-accepted-radio').checked = true;
                    updateRowStatus(rowCounter, 'accepted');
                }
            });
            
            deviceCounter = sampleDevices.length + 1;
        }
        
        // ایجاد datalist برای پیشنهادات
        function createDataLists() {
            // حذف datalist‌های قدیمی اگر وجود دارند
            const oldLists = document.querySelectorAll('datalist');
            oldLists.forEach(list => list.remove());
            
            // ایجاد datalist برای نام دستگاه‌ها
            const deviceNamesList = document.createElement('datalist');
            deviceNamesList.id = 'device-names';
            deviceNames.forEach(name => {
                const option = document.createElement('option');
                option.value = name;
                deviceNamesList.appendChild(option);
            });
            document.body.appendChild(deviceNamesList);
            
            // ایجاد datalist برای سازندگان
            const manufacturersList = document.createElement('datalist');
            manufacturersList.id = 'manufacturers';
            manufacturers.forEach(manufacturer => {
                const option = document.createElement('option');
                option.value = manufacturer;
                manufacturersList.appendChild(option);
            });
            document.body.appendChild(manufacturersList);
        }
        
        // مقداردهی اولیه صفحه
        document.addEventListener('DOMContentLoaded', function() {
            // ایجاد datalist‌ها
            createDataLists();
            
            // ایجاد 3 ردیف اولیه
            const tableBody = document.getElementById('table-body');
            for (let i = 1; i <= 3; i++) {
                tableBody.innerHTML += createRow(i);
            }
            
            // تنظیم تاریخ امروز به صورت خودکار
            const todayPersian = getCurrentPersianDate();
            document.getElementById('inspection-date').value = todayPersian;
            
            // بارگذاری داده‌های ذخیره شده یا نمونه
            const savedData = localStorage.getItem('atratab_medical_qc_v2');
            if (savedData && confirm('آیا می‌خواهید داده‌های ذخیره شده قبلی را بارگذاری کنید؟')) {
                try {
                    const data = JSON.parse(savedData);
                    document.getElementById('medical-center').value = data.medicalCenter || 'بیمارستان امام خمینی';
                    document.getElementById('inspection-date').value = data.inspectionDate || todayPersian;
                    document.getElementById('report-number').value = data.reportNumber || 'QC-MED-1403-001';
                } catch (e) {
                    console.log('خطا در بارگذاری داده‌های ذخیره شده');
                }
            } else if (confirm('آیا می‌خواهید داده‌های نمونه برای نمایش بارگذاری شوند؟')) {
                loadSampleData();
            }
        });
    </script>
</body>
</html>
