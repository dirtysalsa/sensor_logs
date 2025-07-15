Sensor logs
// Print CSV header with timestamp including PM columns
    Serial.println("\ntimestamp,temp_c,humidity_%,pressure_hpa,iaq,co2_ppm,voc_ppm,pm1_0,pm2_5,pm10_0,baseline_ready,spike_detected,signature,total_spikes");
    
    startTime = millis();
    lastReadingTime = startTime;
    lastBsecCall = startTime;
}
