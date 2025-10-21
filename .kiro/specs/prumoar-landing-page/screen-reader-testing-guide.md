# Screen Reader Testing Guide - PrumoAr Landing Page

## Overview

This document provides comprehensive instructions for manually testing the PrumoAr landing page with screen reader software (NVDA, JAWS, or VoiceOver). This testing validates WCAG 2.1 AA compliance for users who rely on assistive technology.

## Prerequisites

### Option 1: NVDA (Free - Windows)
- **Download**: https://www.nvaccess.org/download/
- **Cost**: Free and open source
- **Platform**: Windows only
- **Recommended for**: Initial testing and development

### Option 2: JAWS (Commercial - Windows)
- **Website**: https://www.freedomscientific.com/products/software/jaws/
- **Cost**: Commercial license required (free 40-minute demo available)
- **Platform**: Windows only
- **Recommended for**: Professional/enterprise testing

### Option 3: VoiceOver (Built-in - macOS)
- **Activation**: Cmd + F5 or System Preferences > Accessibility > VoiceOver
- **Cost**: Free (built into macOS)
- **Platform**: macOS only
- **Recommended for**: Mac users and Safari testing

## Testing Setup

1. **Open the landing page** in your preferred browser
   - Chrome, Firefox, or Edge for NVDA/JAWS
   - Safari for VoiceOver (best compatibility)

2. **Launch your screen reader**
   - NVDA: Run NVDA from Start menu
   - JAWS: Run JAWS from Start menu
   - VoiceOver: Press Cmd + F5

3. **Navigate to the page** and prepare to test

## NVDA Testing Instructions

### Basic Navigation Shortcuts

| Shortcut | Action |
|----------|--------|
| `Insert + Down Arrow` | Read from current position to end |
| `Down Arrow` | Read next line |
| `Up Arrow` | Read previous line |
| `H` | Jump to next heading |
| `Shift + H` | Jump to previous heading |
| `K` | Jump to next link |
| `B` | Jump to next button |
| `L` | Jump to next list |
| `I` | Jump to next list item |
| `Insert + F7` | List all elements (headings, links, etc.) |
| `Insert + Space` | Toggle browse/focus mode |

### Testing Checklist

- [ ] **Page Load**: NVDA announces page title "PrumoAr Instalações | Conforto Térmico Profissional"
- [ ] **Skip Link**: Press Tab once - should announce "Pular para o conteúdo principal" link
- [ ] **Skip Link Activation**: Press Enter - focus moves to main content
- [ ] **Logo**: Announces "PrumoAr Instalações - Logotipo da empresa especializada em ar condicionado"
- [ ] **Main Heading**: Press H - announces "Heading level 1: PrumoAr Instalações"
- [ ] **Tagline**: Announces "Profissionais Especializados em Conforto Térmico"
- [ ] **Services Heading**: Press H - announces "Heading level 2: Nossos Serviços de Ar Condicionado"
- [ ] **Services List**: Press L - announces "List with 4 items"
- [ ] **Service Cards**: Each card announces heading level 3 with service name
- [ ] **CTA Heading**: Press H - announces "Heading level 2: Entre em Contato Agora"
- [ ] **WhatsApp Button**: Press K or B - announces "Link: Falar no WhatsApp com PrumoAr"
- [ ] **Email Button**: Press K or B - announces "Link: Enviar e-mail para PrumoAr"
- [ ] **Contact Info**: Phone and email are announced clearly
- [ ] **Footer**: Announces copyright information
- [ ] **Decorative Elements**: Icons with aria-hidden="true" are NOT announced
- [ ] **Focus Order**: Tab order is logical (top to bottom, left to right)

## JAWS Testing Instructions

### Basic Navigation Shortcuts

| Shortcut | Action |
|----------|--------|
| `Insert + Down Arrow` | Say all (read entire page) |
| `Down Arrow` | Read next line |
| `Up Arrow` | Read previous line |
| `H` | Jump to next heading |
| `Shift + H` | Jump to previous heading |
| `Tab` | Jump to next interactive element |
| `Insert + F5` | List all form fields |
| `Insert + F6` | List all headings |
| `Insert + F7` | List all links |
| `Insert + Ctrl + ;` | List all buttons |

### Testing Checklist

- [ ] **Say All**: Press Insert + Down Arrow - entire page reads correctly
- [ ] **Headings List**: Press Insert + F6 - all headings listed hierarchically
- [ ] **Links List**: Press Insert + F7 - all links listed with descriptive text
- [ ] **Landmark Navigation**: Press R - cycles through regions (banner, main, contentinfo)
- [ ] **Interactive Elements**: All buttons and links are reachable via Tab
- [ ] **Alt Text**: All images announce descriptive alternative text
- [ ] **ARIA Labels**: Custom labels are announced correctly
- [ ] **No Orphaned Content**: All content is reachable and announced

## VoiceOver Testing Instructions

### Basic Navigation Shortcuts

| Shortcut | Action |
|----------|--------|
| `VO + A` | Read entire page |
| `VO + Right Arrow` | Move to next item |
| `VO + Left Arrow` | Move to previous item |
| `VO + Cmd + H` | Jump to next heading |
| `VO + Cmd + L` | Jump to next link |
| `VO + Space` | Activate link or button |
| `VO + U` | Open rotor (navigate by element type) |
| `VO + Shift + Down` | Enter group/container |
| `VO + Shift + Up` | Exit group/container |

*Note: VO = Control + Option*

### Testing Checklist

- [ ] **Rotor Navigation**: Press VO + U - can navigate by headings, links, landmarks
- [ ] **Heading Navigation**: VO + Cmd + H cycles through all headings correctly
- [ ] **Link Navigation**: VO + Cmd + L cycles through all links
- [ ] **Landmark Regions**: Rotor shows banner, main, contentinfo regions
- [ ] **Service Cards**: Announced as list items within a list
- [ ] **Button Activation**: VO + Space activates CTA buttons correctly
- [ ] **Focus Indicators**: Visual focus ring visible when navigating
- [ ] **No Trapped Focus**: Can navigate through entire page without getting stuck

## Expected Screen Reader Output

### Page Structure Announcement

```
Banner region
  Image: PrumoAr Instalações - Logotipo da empresa especializada em ar condicionado

Main region
  Heading level 1: PrumoAr Instalações
  Profissionais Especializados em Conforto Térmico
  
  Heading level 2: Nossos Serviços de Ar Condicionado
  List with 4 items
    List item 1
      Heading level 3: Instalação de Ar Condicionado Split
      Instalação profissional com garantia
    List item 2
      Heading level 3: Manutenção e Limpeza
      Manutenção preventiva e corretiva especializada
    List item 3
      Heading level 3: Refrigeração Comercial
      Soluções completas para ambientes comerciais
    List item 4
      Heading level 3: Automação de Fluxo de Ar
      Sistemas inteligentes de climatização
  
  Heading level 2: Entre em Contato Agora
  Solicite um orçamento sem compromisso
  Link: Falar no WhatsApp com PrumoAr
  Link: Enviar e-mail para PrumoAr
  
  Heading level 2: Informações de Contato
  Telefone: mais cinco cinco onze nove oito cinco zero zero zero um um oito
  E-mail: adrianochagas25 arroba hotmail ponto com

Content info region
  Image: PrumoAr Instalações - Logotipo em escala de cinza
  Copyright 2025 PrumoAr Instalações. Todos os direitos reservados.
```

## Common Issues to Check

### ❌ Failures to Look For

1. **Missing Alt Text**: Images announced as "image" or filename
2. **Unclear Links**: Links announced as "click here" or "link"
3. **Skipped Content**: Content not reachable via keyboard/screen reader
4. **Incorrect Heading Levels**: Headings out of order (h1 → h3 without h2)
5. **Decorative Icons Announced**: Icons that should be hidden are read aloud
6. **Unclear Button Labels**: Buttons without descriptive text
7. **Trapped Focus**: Cannot navigate away from an element
8. **Missing Landmarks**: Page structure not clear (no regions)

### ✅ Success Criteria

1. **All content is reachable** via keyboard and screen reader
2. **Headings are hierarchical** (h1 → h2 → h3, no skips)
3. **Links are descriptive** (clear purpose without context)
4. **Images have alt text** (descriptive for content, empty for decorative)
5. **Buttons have labels** (clear action description)
6. **Landmarks are present** (banner, main, contentinfo)
7. **Focus order is logical** (matches visual order)
8. **No content is hidden** unintentionally from screen readers

## Testing Results Template

Use this template to document your testing results:

```markdown
## Screen Reader Testing Results

**Date**: [Date]
**Tester**: [Name]
**Screen Reader**: [NVDA/JAWS/VoiceOver] [Version]
**Browser**: [Browser] [Version]
**Operating System**: [OS] [Version]

### Overall Assessment
- [ ] PASS - All content accessible
- [ ] FAIL - Issues found (see below)

### Detailed Results

#### Page Structure
- [ ] Skip to main content link works
- [ ] All headings announced correctly
- [ ] Heading hierarchy is logical
- [ ] Landmark regions present

#### Content
- [ ] Logo alt text descriptive
- [ ] Service cards announced as list
- [ ] All text content readable
- [ ] Contact information clear

#### Interactive Elements
- [ ] CTA buttons have descriptive labels
- [ ] All links are keyboard accessible
- [ ] Focus order is logical
- [ ] Focus indicators visible

#### ARIA Implementation
- [ ] Decorative icons hidden (aria-hidden)
- [ ] ARIA labels present where needed
- [ ] ARIA roles appropriate
- [ ] Live regions work (if applicable)

### Issues Found
[List any issues discovered during testing]

### Recommendations
[List any suggested improvements]
```

## Automated Pre-Testing

Before manual testing, run these automated checks:

1. **Open browser console** (F12)
2. **Add `?debug` to URL** to enable accessibility logging
3. **Check console output** for:
   - Contrast ratio validation results
   - Keyboard accessibility features confirmation
   - Screen reader testing guide

## Additional Resources

- **NVDA User Guide**: https://www.nvaccess.org/files/nvda/documentation/userGuide.html
- **JAWS Documentation**: https://www.freedomscientific.com/training/jaws/
- **VoiceOver User Guide**: https://support.apple.com/guide/voiceover/welcome/mac
- **WCAG 2.1 Guidelines**: https://www.w3.org/WAI/WCAG21/quickref/
- **WebAIM Screen Reader Testing**: https://webaim.org/articles/screenreader_testing/

## Notes

- **Testing Time**: Allow 15-30 minutes for thorough testing
- **Multiple Screen Readers**: Test with at least 2 different screen readers if possible
- **Real Users**: Consider testing with actual screen reader users for best results
- **Regular Testing**: Re-test after any content or structure changes

---

**Last Updated**: 2025-01-21
**Document Version**: 1.0
