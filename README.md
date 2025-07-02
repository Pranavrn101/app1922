CREATE TABLE public.job_cards (
    id SERIAL,
    mawb_number VARCHAR(50) NOT NULL,
    hawb_number VARCHAR(50),
    importer TEXT,
    exporter TEXT,
    origin VARCHAR(100),
    eta TIMESTAMP WITHOUT TIME ZONE,
    created_date DATE DEFAULT CURRENT_TIMESTAMP,
    defra_required BOOLEAN DEFAULT FALSE,
    attachment_url TEXT,
    status VARCHAR(20) DEFAULT 'Unattended',
    number_of_pieces VARCHAR(100),
    consol_no TEXT,
    shipment_no TEXT,
    CONSTRAINT job_cards_pkey PRIMARY KEY (id),
    CONSTRAINT unique_mawb_number UNIQUE (mawb_number)
);
