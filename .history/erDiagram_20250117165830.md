erDiagram
    ProductInfo {
        INT 機番 PK "機番"
        DATE 日付 PK "日付"
        STRING 品番 PK "品番"
    }
    
    TicketInfo {
        STRING 品番 FK "品番"
        DATE 日付 FK "日付"
        STRING 外観担当者 "外観担当者"
        INT カウンタ数 "カウンタ数"
        INT 検査実績数 "検査実績数"
        FLOAT 単量 "単量"
        BOOLEAN 寸法フラグ "寸法フラグ"
        STRING 備考 "備考"
    }
    
    ProductInfo ||--o{ TicketInfo : "品番と日付で関連付け"