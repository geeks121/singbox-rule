# singbox-rule

Rule sets for sing-box (converted from geeks121/clash_rule).

## Usage

### Local file
```json
{
  "route": {
    "rule_set": [
      {"tag": "youtube", "type": "local", "path": "./rule_set/youtube.json"}
    ],
    "rules": [
      {"rule_set": "youtube", "outbound": "Youtube"}
    ]
  }
}
```

### Remote URL
```json
{
  "route": {
    "rule_set": [
      {"tag": "youtube", "type": "remote", "url": "https://raw.githubusercontent.com/geeks121/singbox-rule/main/youtube.json", "download_detour": "direct"}
    ],
    "rules": [
      {"rule_set": "youtube", "outbound": "Youtube"}
    ]
  }
}
```

## Files
| File | Source | Rules |
|------|--------|-------|
| `youtube.json` | STREAM/rule-youtube.yaml | 175 domain_suffix |
| `whatsapp.json` | SOCIAL/rule-whatsapp.yaml | domain+suffix+keyword+port |
| `sosmed.json` | SOCIAL/rule-sosmed.yaml | Facebook/Messenger domain+ip_cidr |
| `isp.json` | MISC/ISP_ID.yaml | 13 domain_keyword |
| `outlier.json` | MISC/outlier.yaml | 5 rules |
| `game_ml.json` | GAMES/ML.yaml | 22 rules (Mobile Legends) |
| `game_ff.json` | GAMES/freefire.yaml | 40 rules (Free Fire) |
| `game_fc_m.json` | GAMES/fc_m.yaml | 83 rules (FC Mobile) |
| `game_garena.json` | GAMES/garena.yaml | 23 rules (Garena) |
| `reject_yt_udp.json` | inline | reject UDP 443 YouTube |
