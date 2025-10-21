# Screen Reader Testing - Quick Start Guide

## 🚀 Quick Setup (5 minutes)

### Windows Users - NVDA (Free)
1. Download: https://www.nvaccess.org/download/
2. Install and run NVDA
3. Open `index.html` in Chrome/Firefox
4. Press `Insert + Down Arrow` to read the page

### Mac Users - VoiceOver (Built-in)
1. Press `Cmd + F5` to enable VoiceOver
2. Open `index.html` in Safari
3. Press `Control + Option + A` to read the page

## 🎯 Essential Test (2 minutes)

Press these keys in order and verify the output:

| Key | Expected Result |
|-----|----------------|
| `Tab` | "Pular para o conteúdo principal" (Skip link) |
| `Enter` | Jumps to main content |
| `H` | "Heading level 1: PrumoAr Instalações" |
| `H` | "Heading level 2: Nossos Serviços..." |
| `L` | "List with 4 items" |
| `H` | "Heading level 3: Instalação de Ar..." |
| `Tab` (multiple) | Reaches "Falar no WhatsApp" button |
| `Tab` | Reaches "Enviar E-mail" button |

## ✅ Pass Criteria

- [ ] All headings announced
- [ ] Skip link works
- [ ] Service cards in a list
- [ ] Buttons have descriptive labels
- [ ] Contact info reads clearly
- [ ] No content skipped

## 📖 Full Guide

See `screen-reader-testing-guide.md` for complete instructions.

## 🐛 Debug Mode

Add `?debug` to URL to see accessibility logs in console:
```
http://localhost:8000/index.html?debug
```

## 🆘 Common Issues

**"Image" announced instead of description**
→ Check alt text is present

**"Link" without description**
→ Check aria-label on buttons

**Content not reachable**
→ Check tabindex and keyboard navigation

**Icons announced**
→ Check aria-hidden="true" on decorative elements

---

**Need Help?** See full testing guide or contact development team.
