# ovelse
Progoblig 01

overlay(rectangle(240, 20, "solid", "dark blue"),
  rotate(180,
    overlay(rectangle(20, 180, "solid", "dark blue"),
overlay(rectangle(240, 40, "solid", "white"),
    rotate(180,
          overlay(rectangle(40, 180, "solid", "white"),
            rectangle(240, 180, "solid", "fire-brick")))))))

#Progoblig 02; ind 01

fun nordic-flag(inner-cross-h, inner-cross-v, cross-h, cross-v, body):
  frame(
    overlay(rectangle(240, 20, "solid", inner-cross-h),
  rotate(180,
        overlay(rectangle(20, 180, "solid", inner-cross-v),
          overlay(rectangle(240, 40, "solid",cross-h),
    rotate(180,
              overlay(rectangle(40, 180, "solid", cross-v),
                rectangle(240, 180, "solid", body))))))))
end 
nordic-flag(inner-cross-h, inner-cross-v, cross-h, cross-v, body)

#Progoblig 02; ind 02 b

include shared-gdrive("dcic-2021", "1wyQZj_L0qqV9Ekgr9au6RX2iqt2Ga8Ep")
include shared-gdrive("dcic-2021", "1wyQZj_L0qqV9Ekgr9au6RX2iqt2Ga8Ep")
include gdrive-sheets
include data-source
ssid = "1RYN0i4Zx_UETVuYacgaGfnFcv4l9zd9toQTTdkQkj7g"
kWh-wealthy-consumer-data =
  load-table: komponent, energi
    source: load-spreadsheet(ssid).sheet-by-name("kWh", true)
    sanitize energi using string-sanitizer
end
fun energi-to-number(str :: String) -> Number:
  doc: "If s is not a numeric string, default to 0."
  cases(Option) string-to-number(str):
    | some(a) => a
    | none => 0
  end
where:
  energi-to-number("") is 0
  energi-to-number("48") is 48
end
