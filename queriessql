-- =========================================
-- MUSIC STREAMING USER ANALYSIS PROJECT
-- =========================================

-- 1. TABLE CREATION

CREATE TABLE music_streaming (
    user_id TEXT,
    age INTEGER,
    country TEXT,
    subscription_type TEXT,
    device TEXT,
    daily_minutes INTEGER,
    favorite_genre TEXT,
    skip_rate REAL,
    ads_clicked INTEGER,
    churned INTEGER
);

-- 2. DATA INSERTION
-- Buraya kamp boyunca kullandığımız INSERT INTO kodlarını ekleyin.

-- 3. BASIC QUERIES

SELECT *
FROM music_streaming;

SELECT user_id, country, subscription_type, daily_minutes
FROM music_streaming;

SELECT *
FROM music_streaming
WHERE subscription_type = 'premium';

SELECT *
FROM music_streaming
WHERE daily_minutes > 100;

SELECT *
FROM music_streaming
ORDER BY daily_minutes DESC
LIMIT 10;

-- 4. AGGREGATION QUERIES

SELECT COUNT(*) AS total_users
FROM music_streaming;

SELECT SUM(daily_minutes) AS total_daily_minutes
FROM music_streaming;

SELECT AVG(daily_minutes) AS avg_daily_minutes
FROM music_streaming;

-- 5. GROUP BY ANALYSIS

SELECT
    subscription_type,
    COUNT(*) AS user_count,
    SUM(daily_minutes) AS total_daily_minutes,
    AVG(daily_minutes) AS avg_daily_minutes
FROM music_streaming
GROUP BY subscription_type;

SELECT
    churned,
    COUNT(*) AS user_count,
    AVG(daily_minutes) AS avg_daily_minutes,
    AVG(skip_rate) AS avg_skip_rate
FROM music_streaming
GROUP BY churned;

SELECT
    country,
    COUNT(*) AS user_count,
    AVG(daily_minutes) AS avg_daily_minutes
FROM music_streaming
GROUP BY country
ORDER BY avg_daily_minutes DESC;

SELECT
    device,
    COUNT(*) AS user_count,
    AVG(daily_minutes) AS avg_daily_minutes,
    AVG(skip_rate) AS avg_skip_rate
FROM music_streaming
GROUP BY device;

SELECT
    favorite_genre,
    COUNT(*) AS user_count,
    AVG(daily_minutes) AS avg_daily_minutes,
    AVG(skip_rate) AS avg_skip_rate
FROM music_streaming
GROUP BY favorite_genre
ORDER BY avg_skip_rate DESC;

-- 6. DATA QUALITY CHECKS

SELECT *
FROM music_streaming
WHERE skip_rate IS NULL;

SELECT *
FROM music_streaming
WHERE daily_minutes > 300;
