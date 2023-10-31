# ovelse
Progoblig 01

overlay(rectangle(240, 20, "solid", "dark blue"),
  rotate(180,
    overlay(rectangle(20, 180, "solid", "dark blue"),
overlay(rectangle(240, 40, "solid", "white"),
    rotate(180,
          overlay(rectangle(40, 180, "solid", "white"),
            rectangle(240, 180, "solid", "fire-brick")))))))

Progoblig 02; ind 01

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
