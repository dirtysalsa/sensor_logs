Sensor logs

// Print CSV header with timestamp including PM columns

    Serial.println("\ntimestamp,temp_c,humidity_%,pressure_hpa,iaq,co2_ppm,voc_ppm,pm1_0,pm2_5,pm10_0,baseline_ready,spike_detected,signature,total_spikes");
    
    startTime = millis();
    lastReadingTime = startTime;
    lastBsecCall = startTime;
}

The data format changes a bit in the newer versions but it's a logical progression.

The newer logs after we started tracking baseline drift has this structure:

    timestamp,temp_c,humidity_%,pressure_hpa,iaq,co2_ppm,voc_ppm,raw_gas_ohms,pm1_0,pm2_5,pm10_0,baseline_ready,spike_detected,signature,spike_duration_sec,total_spikes,baseline_iaq,baseline_voc,baseline_co2
