# Saptagramctc
Saptagram Computer Training Centre 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Student Admission Application Form</title>
    <style>
        /* A4 Page Layout with Narrow Margins */
        @page {
            size: A4;
            margin: 10mm;
        }
        body {
            font-family: Arial, sans-serif;
            font-size: 12px;
            color: #333;
            margin: 0;
            padding: 0;
            background: #f5f5f5;
        }
        .page-container {
            width: 210mm;
            min-height: 297mm;
            padding: 10mm;
            margin: 10mm auto;
            background: #fff;
            box-sizing: border-box;
            border: 1px solid #ccc;
        }
        h2 {
            text-align: center;
            margin-bottom: 20px;
            font-size: 18px;
            text-transform: uppercase;
            border-bottom: 2px solid #333;
            padding-bottom: 5px;
        }
        fieldset {
            border: 1px solid #999;
            border-radius: 4px;
            padding: 10px 15px;
            margin-bottom: 15px;
        }
        legend {
            font-weight: bold;
            font-size: 13px;
            color: #111;
            padding: 0 5px;
        }
        .form-row {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 10px;
        }
        .form-group {
            flex: 1;
            min-width: 30%;
            display: flex;
            flex-direction: column;
        }
        .form-group.full-width {
            flex-basis: 100%;
        }
        label {
            font-weight: bold;
            margin-bottom: 3px;
            font-size: 11px;
        }
        input[type="text"], input[type="date"], select {
            padding: 5px;
            font-size: 12px;
            border: 1px solid #ccc;
            border-radius: 3px;
        }
        input:focus, select:focus {
            border-color: #0066cc;
            outline: none;
        }
        .radio-group {
            display: flex;
            gap: 15px;
            margin-top: 5px;
        }
        .btn-container {
            text-align: center;
            margin-top: 20px;
        }
        button {
            padding: 8px 16px;
            font-size: 12px;
            font-weight: bold;
            cursor: pointer;
            background-color: #0066cc;
            color: white;
            border: none;
            border-radius: 3px;
            margin: 0 5px;
        }
        button:hover {
            background-color: #004999;
        }
        #preview-section {
            display: none;
            background: #fafafa;
            padding: 10px;
            border: 1px dashed #666;
            margin-bottom: 15px;
        }
        #preview-section h3 {
            margin-top: 0;
            font-size: 14px;
            border-bottom: 1px solid #ddd;
            padding-bottom: 5px;
        }
        .preview-row {
            display: flex;
            margin-bottom: 5px;
        }
        .preview-label {
            font-weight: bold;
            width: 35%;
        }
        .preview-value {
            width: 65%;
        }
        
        /* Print Styles */
        @media print {
            body {
                background: none;
            }
            .page-container {
                margin: 0;
                border: none;
                box-shadow: none;
                width: 100%;
            }
            .btn-container, #form-mode {
                display: none !important;
            }
            #preview-section {
                display: block !important;
                border: none;
                background: none;
                padding: 0;
            }
        }
    </style>
</head>
<body>

<div class="page-container">
    <h2>Student Admission Application Form</h2>
    
    <form id="admissionForm">
        <!-- Student Personal Details -->
        <fieldset>
            <legend>Student's Personal Information</legend>
            <div class="form-row">
                <div class="form-group">
                    <label for="firstName">First Name *</label>
                    <input type="text" id="firstName" required>
                </div>
                <div class="form-group">
                    <label for="middleName">Middle Name</label>
                    <input type="text" id="middleName">
                </div>
                <div class="form-group">
                    <label for="lastName">Last Name *</label>
                    <input type="text" id="lastName" required>
                </div>
            </div>
            
            <div class="form-row">
                <div class="form-group">
                    <label for="dob">Date of Birth *</label>
                    <input type="date" id="dob" required>
                </div>
                <div class="form-group">
                    <label>Gender *</label>
                    <div class="radio-group">
                        <label><input type="radio" name="gender" value="Male" required> Male</label>
                        <label><input type="radio" name="gender" value="Female"> Female</label>
                        <label><input type="radio" name="gender" value="Other"> Other</label>
                    </div>
                </div>
                <div class="form-group">
                    <label for="category">Social Category *</label>
                    <select id="category" required>
                        <option value="">--Select Category--</option>
                        <option value="General">General</option>
                        <option value="OBC">OBC</option>
                        <option value="SC">SC</option>
                        <option value="ST">ST</option>
                        <option value="Other">Other</option>
                    </select>
                </div>
            </div>
        </fieldset>

        <!-- Father's Details -->
        <fieldset>
            <legend>Father's Information</legend>
            <div class="form-row">
                <div class="form-group">
                    <label for="fatherFirstName">First Name *</label>
                    <input type="text" id="fatherFirstName" required>
                </div>
                <div class="form-group">
                    <label for="fatherMiddleName">Middle Name</label>
                    <input type="text" id="fatherMiddleName">
                </div>
                <div class="form-group">
                    <label for="fatherLastName">Last Name *</label>
                    <input type="text" id="fatherLastName" required>
                </div>
            </div>
        </fieldset>

        <!-- Mother's Details -->
        <fieldset>
            <legend>Mother's Information</legend>
            <div class="form-row">
                <div class="form-group">
                    <label for="motherFirstName">First Name *</label>
                    <input type="text" id="motherFirstName" required>
                </div>
                <div class="form-group">
                    <label for="motherMiddleName">Middle Name</label>
                    <input type="text" id="motherMiddleName">
                </div>
                <div class="form-group">
                    <label for="motherLastName">Last Name *</label>
                    <input type="text" id="motherLastName" required>
                </div>
            </div>
        </fieldset>
    </form>

    <!-- Preview Container -->
    <div id="preview-section">
        <h3>Application Preview</h3>
        <div id="preview-content"></div>
    </div>

    <!-- Action Buttons -->
    <div class="btn-container">
        <button type="button" id="previewBtn" onclick="generatePreview()">Preview Form</button>
        <button type="button" id="submitPrintBtn" style="display:none;" onclick="finalSubmitAndPrint()">Final Submit & Print</button>
    </div>
</div>

<script>
    function generatePreview() {
        const form = document.getElementById('admissionForm');
        if (!form.checkValidity()) {
            form.reportValidity();
            return;
        }

        const data = {
            "Student Name": `${document.getElementById('firstName').value} ${document.getElementById('middleName').value} ${document.getElementById('lastName').value}`,
            "Date of Birth": document.getElementById('dob').value,
            "Gender": document.querySelector('input[name="gender"]:checked').value,
            "Social Category": document.getElementById('category').value,
            "Father's Name": `${document.getElementById('fatherFirstName').value} ${document.getElementById('fatherMiddleName').value} ${document.getElementById('fatherLastName').value}`,
            "Mother's Name": `${document.getElementById('motherFirstName').value} ${document.getElementById('motherMiddleName').value} ${document.getElementById('motherLastName').value}`
        };

        let html = '';
        for (const [key, value] of Object.entries(data)) {
            html += `<div class="preview-row"><div class="preview-label">${key}:</div><div class="preview-value">${value.replace(/\s+/g, ' ')}</div></div>`;
        }

        document.getElementById('preview-content').innerHTML = html;
        document.getElementById('admissionForm').style.display = 'none';
        document.getElementById('preview-section').style.display = 'block';
        document.getElementById('previewBtn').style.display = 'none';
        document.getElementById('submitPrintBtn').style.display = 'inline-block';
    }

    function finalSubmitAndPrint() {
        window.print();
    }
</script>

</body>
</html>
