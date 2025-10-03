# my-website
-# Retry creating the site bundle and zip.
import os, shutil, zipfile, textwrap, pathlib

workdir = "/mnt/data/event_site_safari"
os.makedirs(workdir, exist_ok=True)

src_image = "/mnt/data/5F074257-2392-4737-8F2C-50F306E86AD0.jpeg"
dst_image = os.path.join(workdir, "poster.jpeg")
shutil.copyfile(src_image, dst_image)

html_content = """<!doctype html>
<html lang="en" dir="ltr">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Cybersecurity Event — Demo</title>
<style>
  /* Safari-friendly simple styles */
  html,body{height:100%;margin:0;font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial;}
  body{background:#000;color:#fff;overflow:hidden}
  .screen{position:fixed;inset:0;display:flex;align-items:center;justify-content:center;background:#000;transition:opacity .6s ease;z-index:10}
  .ransom{max-width:1000px;padding:28px;border-radius:6px;background:linear-gradient(180deg,#0b0b0b,#000);box-shadow:0 12px 40px rgba(0,0,0,.6);border:3px solid rgba(255,0,0,.12)}
  .ransom h1{margin:0;color:#ff3b3b;font-size:36px;letter-spacing:2px}
  .ransom p{margin:12px 0;color:#ffd7d7;font-size:18px}
  .count{font-family:monospace;color:#fff;background:rgba(255,255,255,.03);padding:10px;border-radius:6px;display:inline-block;margin-top:8px}
  /* reveal area */
  .reveal{position:fixed;inset:0;background:#111;display:flex;align-items:flex-start;justify-content:center;overflow:auto;padding:28px;box-sizing:border-box}
  .card{max-width:960px;width:100%;background:linear-gradient(180deg,#071226,#051018);border-radius:10px;padding:18px;border:1px solid rgba(255,255,255,0.04);color:#dcefe6;box-shadow:0 10px 30px rgba(0,0,0,.6)}
  .card h2{margin:0 0 6px 0;color:#8ff7ff;font-size:28px}
  .meta{color:#bcd8d1;margin-bottom:12px}
  .desc{color:#cfe9e1;line-height:1.5}
  .note{margin-top:12px;padding:8px;background:rgba(255,255,255,0.02);border-radius:6px;color:#a9a9a9;font-size:13px}
  .poster{margin-top:14px;border-radius:6px;overflow:hidden;border:1px solid rgba(255,255,255,0.03)}
  .cta{display:inline-block;margin-top:12px;padding:10px 14px;border-radius:8px;background:#8ff7ff;color:#001;font-weight:700;text-decoration:none}
  /* small screen tweaks */
  @media (max-width:520px){
    .ransom h1{font-size:28px}
