---
name: Clickable Tiles for What's New
---
<HTMLBlock>{`
<style>
    .card-container {
        display: flex;
        gap: 20px;
    }

    .card {
        display: flex;
        align-items: center;
        gap: 15px;
        border: 1px solid #B2B7B9;
        border-radius: 10px;
        padding: 20px 25px;
        background-color: #fff;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        width: 300px;
        transition: box-shadow 0.3s ease;
        text-decoration: none;
        color: inherit;
    }

    .card:hover {
        box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
        cursor: pointer;
    }

    .card-icon {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 50px;
        height: 50px;
    }

    .card-icon img {
        width: 100%;
        height: 100%;
    }

    .divider {
        border-left: 1px solid #B2B7B9;
        height: 40px;
    }

    .card-content {
        display: flex;
        flex-direction: column;
        gap: 4px;
    }

    .card-title {
        font-size: 15px;
        font-weight: bold;
        color: #222;
    }

    .card-description {
        font-size: 14px;
        color: #B2B7B9;
    }
</style>
</head>
<body>
    <div class="card-container">
        <a href="https://docs.clevertap.com/docs/events-changelog" class="card" target="_blank">
            <div class="card-icon">
                <img src="https://files.readme.io/b2a942b44fb9852a74dd10f4d503100a127e6853ad209936d52bfb6e3ea61bd8-Schema.svg" alt="Changelog Icon">
            </div>
            <div class="divider"></div>
            <div class="card-content">
                <div class="card-title">Events Changelog</div>
                <div class="card-description">System Event Additions & Updates</div>
            </div>
        </a>

        <a href="https://developer.clevertap.com/docs/changelog" class="card" target="_blank">
            <div class="card-icon">
                <img src="https://files.readme.io/4d7a89d59bce8d11fe6851082a3db311e3f627e572530136edfa89ebb4d334d9-fi_16627473.svg" alt="SDK Changelog Icon">
            </div>
            <div class="divider"></div>
            <div class="card-content">
                <div class="card-title">SDK Changelog</div>
                <div class="card-description">Platform SDK Changelog</div>
            </div>
        </a>
    </div>
</body>
`}</HTMLBlock>
